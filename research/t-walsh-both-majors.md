# 1♣–1NT showing both majors

Research checked 8 October 2026. This supplements the
[survey of direct 1NT responses](t-walsh-1nt-response.md). It records sources
and design implications; it does not change Muscat's system agreements.

## What IntoBridge actually documents

**IntoBridge's current T-Walsh settings describe 6–10 with exactly four
hearts and four spades.** That is narrower than the reported 4+♥, 4+♠
treatment: its help text explicitly says
“Exactly four hearts and four spades, 6-10; stronger 4-4 hands bid 1!D”.
Here `!D` is IntoBridge's diamond-symbol notation. The primary source is
the site's public settings bundle, under the question
`t_walsh_one_nt_response`, option `both_majors_weak`.
[IntoBridge settings source](https://play.intobridge.com/4636.8a7d660695a46547.js).

The surrounding T-Walsh help routes 5♠–4♥ and 5–5 through the 1♥ response;
1♠ carries hands without a four-card major. This supports reading the weak
1NT option as exactly 4–4, rather than shorthand for every two-major hand.
The same source offers a natural invitational 1NT as an alternative option.
[IntoBridge settings source, `walsh` and `t_walsh_one_nt_response`](https://play.intobridge.com/4636.8a7d660695a46547.js).

This is a verified description of the **published settings**, not a test of
the robot's actual hand selection. If an in-play alert says 4+4+, that would
be a discrepancy worth checking against a particular auction and selected
system; these sources alone do not resolve it.

Lia supports multiple selectable systems. IntoBridge identifies Lia as its
own robot, developed since summer 2023, and says each system's convention
card is available from Game Preferences. Thus “Lia plays…” needs the system
and custom settings attached to it. The older default 2/1 cards do not
document every later custom option.
[Official FAQ, “Who is LIA?” and “What systems can I play?”](https://intobridge.com/news/faq-frequently-asked-questions/).

### Source access and limits

The current [IntoBridge application](https://play.intobridge.com/) serves
the linked JavaScript asset through its public build. It was downloaded
directly and searched for the named settings above. The URL contains a build
hash and may disappear after a deployment; the question and option keys
identify the text in a later build. No account preferences were changed.

The dedicated both-major entry supplies **no continuation table**. I did not
find a primary-source explanation of these follow-ups:

| After 1♣–1NT | Still unverified for Lia's both-major option |
| --- | --- |
| Pass | Whether opener may pass with a minimum and no major fit. |
| 2♣ | Natural clubs or an artificial enquiry; forcing status. |
| 2♦ | Natural, strength-showing, or an enquiry; forcing status. |
| 2♥ / 2♠ | Required support and strength; whether responder can continue. |
| 2NT / 3M / 3NT | Exact strength ranges and forcing status. |
| Responder's next call | Any shape/strength answers, invitation acceptance, or signoff rules. |

A separate generic setting describes several possible meanings of
1m–1NT–2NT. It does not explain its interaction with this artificial response.
Likewise, the adjacent T-Walsh acceptance settings concern **1♣–1♦/1♥**,
not **1♣–1NT**. Neither supplies a verified answer table for this auction.
[IntoBridge settings source, `one_minor_one_nt_two_nt` and `t_walsh_acceptance`](https://play.intobridge.com/4636.8a7d660695a46547.js).

## Implications for Muscat — analysis, not Lia's continuations

The initial choice is **exactly 4–4 versus at least 4–4**. The narrower
version removes the need to discover a fifth major on responder's next turn.
An extended 4+4+ version would also accommodate 5–4 and perhaps 5–5 hands,
so finding the longer major becomes another job for the continuations.

The benefit is immediate disclosure of both majors and limited strength.
Opener can select a known four-four fit in one bid, and would declare that
major because responder has bid neither major. If the eventual contract is
notrump, responder declares because responder first bid notrump.

A major fit is not guaranteed. For example, in ♠♥♦♣ order, a 3=3=3=4 opener
opposite a 4=4=3=2 responder has only seven cards in either major. Muscat's
weak balanced opening hands can have this shape. Consequently the minimum
no-fit branch needs as much attention as the easy four-card-support branch.
[Muscat opening structure](../src/Openings.md).

A manageable agreement would need to settle these points explicitly:

- **Minimum with no fit:** is 1NT passable, and when should opener prefer
  natural clubs? Making the response forcing removes the option of stopping
  in 1NT; that needs a deliberate reason.
- **2M support:** with the exact 4–4 version, three-card support means choosing
  a seven-card fit. If 2M instead promises four, it should say so. With 4+4+,
  define how to find a five-three fit before settling for four-three.
- **Strong opener:** distinguish Muscat's 18–20 balanced hands from its
  12–14 hands, and provide an invitation or forcing route for strong
  unbalanced hands. The ordinary major-transfer 1NT rebid does not supply
  this distinction after responder has already bid 1NT.
- **Responder's remaining ranges:** retain a transfer route for hands below
  six and above ten. If using exact 4–4, the 5–4 and 5–5 hands also remain
  in the transfer structure. Muscat currently allows 0+ major responses.
  [Current responses](../src/1C.md).
- **Invitations and enquiries:** reserve any artificial 2♣/2♦ call only after
  assigning the natural club exit and minimum no-fit hands, and then define
  every answer. A named enquiry without answers is not a complete method.

The evidence supports investigating **6–10, exactly 4–4** as a concrete
alternative to the club-transfer and GF-relay uses of 1NT. It does not yet
support copying a continuation scheme and calling it Lia's. The decision
between these uses should follow the priority: organizing weak two-major
hands, organizing club hands, or describing game-forcing hands by relay.

### A possible natural starting structure for exact 4–4

The following is a **Muscat design proposal**, not a sourced Lia agreement
or a complete system. It assumes 1NT is nonforcing and exactly 4–4.

| Opener after 1♣–1NT | Proposed meaning |
| --- | --- |
| Pass | Minimum, no four-card major, content to play 1NT. |
| 2♣ | Natural long clubs, nonforcing; normally six or more. |
| 2♥ / 2♠ | Four-card fit, to play. |
| 2NT | Natural invitation, no four-card major. |
| 3♥ / 3♠ | Invitation with a four-card fit. |
| 3NT / 4♥ / 4♠ | Choice of game. |

Responder passes the signoffs and accepts or declines invitations on hand
evaluation within 6–10. This gives the common partscore and invitation
auctions simple meanings without a shape relay. Muscat's 18–20 balanced
opener must choose an invitation or game according to strength and fit;
it cannot use the same minimum signoff as a 12–14 hand.

Before adoption, define 2♦, strong club hands, slam exploration and
interference, and calibrate the invitation ranges. In particular, the table
deliberately leaves the forcing route unresolved. If responder may instead
have **4+4+**, this skeleton is insufficient: passing with three-card major
support may miss a five-three fit, and a length enquiry or another agreed
way to locate that fit becomes useful.

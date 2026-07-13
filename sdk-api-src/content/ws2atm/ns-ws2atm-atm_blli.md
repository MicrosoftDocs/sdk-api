---
UID: NS:ws2atm.ATM_BLLI
title: ATM_BLLI (ws2atm.h)
description: The ATM_BLLI structure is used to identify B-LLI information for an associated ATM socket.
helpviewer_keywords: ["ATM_BLLI","ATM_BLLI structure [Winsock]","_win32_atm_blli_2","winsock.atm_blli_2","ws2atm/ATM_BLLI"]
old-location: winsock\atm_blli_2.htm
tech.root: WinSock
ms.assetid: 15f600eb-8a73-4bb4-9405-8c6ea9b6ea8a
ms.date: 12/05/2018
ms.keywords: ATM_BLLI, ATM_BLLI structure [Winsock], _win32_atm_blli_2, winsock.atm_blli_2, ws2atm/ATM_BLLI
req.header: ws2atm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ATM_BLLI
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ATM_BLLI
 - ws2atm/ATM_BLLI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2atm.h
api_name:
 - ATM_BLLI
---

# ATM_BLLI structure


## -description

The 
<b>ATM_BLLI</b> structure is used to identify B-LLI information for an associated ATM socket.

## -struct-fields

### -field Layer2Protocol

Identifies the layer-two protocol. Corresponds to the <i>User information layer 2 protocol</i> field in the B-LLI information element. A value of SAP_FIELD_ABSENT indicates that this field is not used, and a value of SAP_FIELD_ANY means wildcard.

### -field Layer2UserSpecifiedProtocol

Identifies the user-specified layer-two protocol. Only used if the <b>Layer2Protocol</b> parameter is set to BLLI_L2_USER_SPECIFIED. The valid values range from zero–127. Corresponds to the <i>User specified layer 2 protocol information</i> field in the B-LLI information element.

### -field Layer3Protocol

Identifies the layer-three protocol. Corresponds to the <i>User information layer 3 protocol</i> field in the B-LLI information element. A value of SAP_FIELD_ABSENT indicates that this field is not used, and a value of SAP_FIELD_ANY means wildcard.

### -field Layer3UserSpecifiedProtocol

Identifies the user-specified layer-three protocol. Only used if the <b>Layer3Protocol</b> parameter is set to BLLI_L3_USER_SPECIFIED. The valid values range from zero–127. Corresponds to the <i>User specified layer 3 protocol information</i> field in the B-LLI information element.

### -field Layer3IPI

Identifies the layer-three Initial Protocol Identifier. Only used if the <b>Layer3Protocol</b> parameter is set to BLLI_L3_ISO_TR9577. Corresponds to the <i>ISO/IEC TR 9577 Initial Protocol Identifier</i> field in the B-LLI information element.

### -field SnapID

Identifies the 802.1 SNAP identifier. Only used if the <b>Layer3Protocol</b> parameter is set to BLLI_L3_ISO_TR9577 and <b>Layer3IPI</b> is set to BLLI_L3_IPI_SNAP, indicating an IEEE 802.1 SNAP identifier. Corresponds to the <i>OUI</i> and <i>PID</i> fields in the B-LLI information element.

## -remarks

The following are the manifest constants associated with the 
<b>ATM_BLLI</b> structure:


```cpp
#include <windows.h>

/* 
 *  values used for Layer2Protocol in struct B-LLI
 */
#define BLLI_L2_ISO_1745           0x01   /* Basic mode ISO 1745    */
#define BLLI_L2_Q921               0x02   /* CCITT Rec. Q.921       */
#define BLLI_L2_X25L               0x06   /* CCITT Rec. X.25, link layer              */
#define BLLI_L2_X25M               0x07   /* CCITT Rec. X.25, multilink               */
#define BLLI_L2_ELAPB              0x08   /* Extended LAPB; for half duplex operation */
#define BLLI_L2_HDLC_NRM           0x09   /* HDLC NRM (ISO 4335)                      */
#define BLLI_L2_HDLC_ABM           0x0A   /* HDLC ABM (ISO 4335)                      */
#define BLLI_L2_HDLC_ARM           0x0B   /* HDLC ARM (ISO 4335)                      */
#define BLLI_L2_LLC                0x0C   /* LAN logical link control (ISO 8802/2)    */
#define BLLI_L2_X75                0x0D   /* CCITT Rec. X.75, single link procedure   */
#define BLLI_L2_Q922               0x0E   /* CCITT Rec. Q.922                         */
#define BLLI_L2_USER_SPECIFIED     0x10   /* User Specified                           */
#define BLLI_L2_ISO_7776           0x11   /* ISO 7776 DTE-DTE operation               */

/* 
 *  values used for Layer3Protocol in struct B-LLI
 */
#define BLLI_L3_X25                0x06   /* CCITT Rec. X.25, packet layer            */
#define BLLI_L3_ISO_8208           0x07   /* ISO/IEC 8208 (X.25 packet layer for DTE  */
#define BLLI_L3_X223               0x08   /* X.223/ISO 8878                           */
#define BLLI_L3_SIO_8473           0x09   /* ISO/IEC 8473 (OSI connectionless)        */
#define BLLI_L3_T70                0x0A   /* CCITT Rec. T.70 min. network layer       */
#define BLLI_L3_ISO_TR9577         0x0B   /* ISO/IEC TR 9577 Network Layer Protocol ID*/
#define BLLI_L3_USER_SPECIFIED     0x10   /* User Specified                           */

/* 
 *  values used for Layer3IPI in struct B-LLI
 */
#define BLLI_L3_IPI_SNAP           0x80   /* IEEE 802.1 SNAP identifier               */
#define BLLI_L3_IPI_IP             0xCC   /* Internet Protocol (IP) identifier        */

```

## -see-also

<a href="/windows/desktop/api/ws2atm/ns-ws2atm-atm_address">ATM_ADDRESS</a>



<a href="/windows/desktop/api/ws2atm/ns-ws2atm-atm_bhli">ATM_BHLI</a>



<a href="/windows/desktop/api/ws2atm/ns-ws2atm-sockaddr_atm">sockaddr_atm</a>


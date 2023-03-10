---
UID: NS:ws2atm.ATM_BHLI
title: ATM_BHLI (ws2atm.h)
description: The ATM_BHLI structure is used to identify B-HLI information for an associated ATM socket.
helpviewer_keywords: ["ATM_BHLI","ATM_BHLI structure [Winsock]","ATM_BHLI_IE","_win32_atm_bhli_2","winsock.atm_bhli_2","ws2atm/ATM_BHLI"]
old-location: winsock\atm_bhli_2.htm
tech.root: WinSock
ms.assetid: a7e09a8e-5990-4493-bd73-016363b57427
ms.date: 12/05/2018
ms.keywords: ATM_BHLI, ATM_BHLI structure [Winsock], ATM_BHLI_IE, _win32_atm_bhli_2, winsock.atm_bhli_2, ws2atm/ATM_BHLI
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
req.typenames: ATM_BHLI
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ATM_BHLI
 - ws2atm/ATM_BHLI
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
 - ATM_BHLI
---

# ATM_BHLI structure


## -description

The 
<b>ATM_BHLI</b> structure is used to identify B-HLI information for an associated ATM socket.

## -struct-fields

### -field HighLayerInfoType

Identifies the <b>high layer information type</b> field in the B-LLI information element. Note that the type <b>BHLI_HighLayerProfile</b> has been eliminated in UNI 3.1. A value of SAP_FIELD_ABSENT indicates that B-HLI is not present, and a value of SAP_FIELD_ANY means wildcard.

### -field HighLayerInfoLength

Identifies the number of bytes from one to eight in the <b>HighLayerInfo</b> array. Valid values include eight for the cases of BHLI_ISO and BHLI_UserSpecific, four for BHLI_HighLayerProfile, and seven for BHLI_VendorSpecificAppId.

### -field HighLayerInfo

Identifies the <b>high layer information</b> field in the B-LLI information element. In the case of <b>HighLayerInfoType</b> being BHLI_VendorSpecificAppId, the first 3 bytes consist of a globally-administered organizationally unique identifier (OUI), (according to IEEE standard 802-1990), followed by a 4-byte application identifier, which is administered by the vendor identified by the OUI. Value for the case of BHLI_UserSpecific is user defined and requires bilateral agreement between two end users.

## -remarks

The following are the manifest constants associated with the 
<b>ATM_BHLI</b> structure:


```cpp
#include <windows.h>
/* 
 *  values used for the HighLayerInfoType field in struct ATM_BHLI
 */

#define BHLI_ISO                   0x00   /* ISO                                 */
#define BHLI_UserSpecific          0x01   /* User Specific                       */
#define BHLI_HighLayerProfile      0x02   /* High layer profile (only in UNI3.0) */
#define BHLI_VendorSpecificAppId   0x03   /* Vendor-Specific Application ID      */

```

## -see-also

<a href="/windows/desktop/api/ws2atm/ns-ws2atm-atm_address">ATM_ADDRESS</a>



<a href="/windows/desktop/api/ws2atm/ns-ws2atm-atm_blli">ATM_BLLI</a>



<a href="/windows/desktop/api/ws2atm/ns-ws2atm-sockaddr_atm">sockaddr_atm</a>


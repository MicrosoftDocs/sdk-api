---
UID: NS:ws2atm.ATM_BHLI
title: ATM_BHLI
author: windows-driver-content
description: The ATM_BHLI structure is used to identify B-HLI information for an associated ATM socket.
old-location: winsock\atm_bhli_2.htm
old-project: WinSock
ms.assetid: a7e09a8e-5990-4493-bd73-016363b57427
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ATM_BHLI, ATM_BHLI structure [Winsock], ATM_BHLI_IE, _win32_atm_bhli_2, winsock.atm_bhli_2, ws2atm/ATM_BHLI
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ws2atm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ATM_BHLI
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ws2atm.h
api_name:
-	ATM_BHLI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
/* 
 *  values used for the HighLayerInfoType field in struct ATM_BHLI
 */

#define BHLI_ISO                   0x00   /* ISO                                 */
#define BHLI_UserSpecific          0x01   /* User Specific                       */
#define BHLI_HighLayerProfile      0x02   /* High layer profile (only in UNI3.0) */
#define BHLI_VendorSpecificAppId   0x03   /* Vendor-Specific Application ID      */
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544051">ATM_ADDRESS</a>



<a href="https://msdn.microsoft.com/15f600eb-8a73-4bb4-9405-8c6ea9b6ea8a">ATM_BLLI</a>



<a href="https://msdn.microsoft.com/6cbeb19f-0aa8-48a1-a46a-691edc542d5a">sockaddr_atm</a>
 

 


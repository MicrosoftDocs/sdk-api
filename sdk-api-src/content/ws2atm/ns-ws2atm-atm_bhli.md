---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


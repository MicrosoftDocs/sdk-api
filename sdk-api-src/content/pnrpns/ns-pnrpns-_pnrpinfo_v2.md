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

# _PNRPINFO_V2 structure


## -description


The <b>PNRPINFO_V1</b> structure  is pointed to by the <b>lpBlob</b> member of the <a href="https://msdn.microsoft.com/e0af2cd9-9cbf-44a1-aa4d-4df211b04782">WSAQUERYSET</a> structure.


## -struct-fields




### -field dwSize

Specifies the size of this structure.


### -field lpwszIdentity

Points  to the Unicode string that contains the identity.


### -field nMaxResolve

Specifies the requested number of resolutions.


### -field dwTimeout

Specifies the time, in seconds, to wait for a response.


### -field dwLifetime

Specifies the number of seconds between refresh operations. Must be   86400 (24 * 60 * 60 seconds).


### -field enResolveCriteria

Specifies the criteria used to resolve matches.  PNRP can look for the first matching name, or attempt to find a name that is numerically close to the service location. Valid values are specified by <a href="https://msdn.microsoft.com/11104d6c-75a8-454a-8203-b1ef105db61a">PNRP_RESOLVE_CRITERIA</a>.


### -field dwFlags

Specifies the flags to use for the resolve operation. The valid value is:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>PNRPINFO_HINT</td>
<td>Indicates that the <b>saHint</b> member is used. The hint influences how the service location portion of the PNRP ID is generated; it also influences how names are resolved, and specifies how to select between multiple peer names.</td>
</tr>
</table>
 


### -field saHint

Specifies the IPv6 address to  use for the location. The  <b>dwFlags</b> member must be PNRPINFO_HINT.


### -field enNameState

Specifies the state of the registered ID.  This value is reserved and must be set to zero (0).


### -field enExtendedPayloadType

 


### -field blobPayload

 


### -field pwszPayload

 




## -remarks



 Starting with Windows Vista, please use the <a href="https://msdn.microsoft.com/7f137de6-28ab-4f16-9009-a73f949fb3ec">PNRPINFO_V2</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/e92ecb14-3f3a-48bb-963b-0c6e58c54089">PNRP and
			 BLOB</a>



<a href="https://msdn.microsoft.com/0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b">PNRP and
			 WSAQUERYSET</a>



<a href="https://msdn.microsoft.com/7f137de6-28ab-4f16-9009-a73f949fb3ec">PNRPINFO_V2</a>



<a href="https://msdn.microsoft.com/e0af2cd9-9cbf-44a1-aa4d-4df211b04782">WSAQUERYSET</a>
 

 


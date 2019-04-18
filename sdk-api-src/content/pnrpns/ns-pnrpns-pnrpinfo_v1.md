---
UID: NS:pnrpns._PNRPINFO_V1
title: PNRPINFO_V1 (pnrpns.h)
author: windows-sdk-content
description: The PNRPINFO_V1 structure is pointed to by the lpBlob member of the WSAQUERYSET structure.
old-location: p2p\pnrpinfo.htm
tech.root: P2PSdk
ms.assetid: 02031191-3682-45f6-a6c5-8546153bc681
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPNRPINFO_V1, PNRPINFO, PNRPINFO structure [Peer Networking], PNRPINFO_V1, PNRPINFO_V1 structure [Peer Networking], PPNRPINFO, PPNRPINFO structure pointer [Peer Networking], PPNRPINFO_V1, PPNRPINFO_V1 structure pointer [Peer Networking], p2p.pnrpinfo, pnrpns/PNRPINFO, pnrpns/PNRPINFO_V1, pnrpns/PPNRPINFO, pnrpns/PPNRPINFO_V1"
ms.topic: struct
req.header: pnrpns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pnrpns.h
api_name:
 - PNRPINFO_V1
product: Windows
targetos: Windows
req.typenames: PNRPINFO_V1, *PPNRPINFO_V1
req.redist: 
ms.custom: 19H1
---

# PNRPINFO_V1 structure


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


## -remarks



 Starting with Windows Vista, please use the <a href="https://msdn.microsoft.com/7f137de6-28ab-4f16-9009-a73f949fb3ec">PNRPINFO_V2</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/e92ecb14-3f3a-48bb-963b-0c6e58c54089">PNRP and
			 BLOB</a>



<a href="https://msdn.microsoft.com/0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b">PNRP and
			 WSAQUERYSET</a>



<a href="https://msdn.microsoft.com/7f137de6-28ab-4f16-9009-a73f949fb3ec">PNRPINFO_V2</a>



<a href="https://msdn.microsoft.com/e0af2cd9-9cbf-44a1-aa4d-4df211b04782">WSAQUERYSET</a>
 

 


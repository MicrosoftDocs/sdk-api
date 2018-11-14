---
UID: NF:mfidl.IMFOutputPolicy.GetOriginatorID
title: IMFOutputPolicy::GetOriginatorID
author: windows-sdk-content
description: Retrieives a GUID identifying the input trust authority (ITA) that created this output policy object.
old-location: mf\imfoutputpolicy_getoriginatorid.htm
tech.root: medfound
ms.assetid: 3412bb81-c4b8-4e10-9a8e-8eae413ca82d
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 3412bb81-c4b8-4e10-9a8e-8eae413ca82d, GetOriginatorID, GetOriginatorID method [Media Foundation], GetOriginatorID method [Media Foundation],IMFOutputPolicy interface, IMFOutputPolicy interface [Media Foundation],GetOriginatorID method, IMFOutputPolicy.GetOriginatorID, IMFOutputPolicy::GetOriginatorID, mf.imfoutputpolicy_getoriginatorid, mfidl/IMFOutputPolicy::GetOriginatorID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFOutputPolicy.GetOriginatorID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFOutputPolicy.GetOriginatorID
: 
---

# IMFOutputPolicy::GetOriginatorID


## -description



Retrieives a GUID identifying the input trust authority (ITA) that created this output policy object.




## -parameters




### -param pguidOriginatorID [out]

Receives a GUID that identifies the originating ITA.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



All of the policy objects and output schemas from the same ITA should return the same originator identifier (including dynamic policy changes). This value enables the OTA to distinguish policies that originate from different ITAs, so that the OTA can update dynamic policies correctly.




## -see-also




<a href="https://msdn.microsoft.com/76af8e03-9584-4f4b-ab2c-8a0ff2c3485b">IMFOutputPolicy</a>
 

 


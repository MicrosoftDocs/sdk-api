---
UID: NF:mfidl.IMFOutputSchema.GetOriginatorID
title: IMFOutputSchema::GetOriginatorID
author: windows-sdk-content
description: Retrieves a GUID identifying the input trust authority (ITA) that generated this output schema object.
old-location: mf\imfoutputschema_getoriginatorid.htm
tech.root: medfound
ms.assetid: a8e7ccbe-8fcf-418e-b3e8-263f6296ff36
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetOriginatorID, GetOriginatorID method [Media Foundation], GetOriginatorID method [Media Foundation],IMFOutputSchema interface, IMFOutputSchema interface [Media Foundation],GetOriginatorID method, IMFOutputSchema.GetOriginatorID, IMFOutputSchema::GetOriginatorID, a8e7ccbe-8fcf-418e-b3e8-263f6296ff36, mf.imfoutputschema_getoriginatorid, mfidl/IMFOutputSchema::GetOriginatorID
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
 - IMFOutputSchema.GetOriginatorID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFOutputSchema::GetOriginatorID


## -description



Retrieves a GUID identifying the input trust authority (ITA) that generated this output schema object.




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




<a href="https://msdn.microsoft.com/d0786628-dde9-43a9-8e81-0b0c396ad426">IMFOutputSchema</a>
 

 


---
UID: NF:wmcontainer.IMFASFProfile.GetStreamByNumber
title: IMFASFProfile::GetStreamByNumber
author: windows-sdk-content
description: Retrieves an Advanced Systems Format (ASF) stream configuration object for a stream in the profile. This method references the stream by stream number instead of stream index.
old-location: mf\imfasfprofile_getstreambynumber.htm
old-project: medfound
ms.assetid: 1e3fadf0-1549-4d51-b263-727b15c55023
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 1e3fadf0-1549-4d51-b263-727b15c55023, GetStreamByNumber, GetStreamByNumber method [Media Foundation], GetStreamByNumber method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],GetStreamByNumber method, IMFASFProfile.GetStreamByNumber, IMFASFProfile::GetStreamByNumber, mf.imfasfprofile_getstreambynumber, wmcontainer/IMFASFProfile::GetStreamByNumber
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: MFSINK_WMDRMACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFProfile.GetStreamByNumber
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFProfile::GetStreamByNumber


## -description



Retrieves an Advanced Systems Format (ASF) stream configuration object for a stream in the profile. This method references the stream by stream number instead of stream index.




## -parameters




### -param wStreamNumber [in]

The stream number for which to obtain the interface pointer.


### -param ppIStream [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a> interface of the ASF stream configuration object. The caller must release the interface.


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



This method does not create a copy of the stream configuration object. The pointer that is retrieved points to the object within the profile object. You must not make any changes to the stream configuration object using this pointer, because doing so can affect the profile object in unexpected ways.

To change the configuration of the stream configuration object in the profile, you must first clone the stream configuration object by calling <a href="https://msdn.microsoft.com/c87d658f-6569-464b-a9d0-487d44f76cc0">IMFASFStreamConfig::Clone</a>. Make whatever changes are required to the clone of the object and then add the updated object by calling the <a href="https://msdn.microsoft.com/c2272260-74ab-42ff-bff3-d6c6d5b322f3">IMFASFProfile::SetStream</a> method.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/918f6534-811e-42f6-9836-1c77816007fa">IMFASFProfile::GetStream</a>



<a href="https://msdn.microsoft.com/c2272260-74ab-42ff-bff3-d6c6d5b322f3">IMFASFProfile::SetStream</a>



<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>
 

 


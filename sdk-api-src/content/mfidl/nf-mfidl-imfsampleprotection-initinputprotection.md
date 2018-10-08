---
UID: NF:mfidl.IMFSampleProtection.InitInputProtection
title: IMFSampleProtection::InitInputProtection
author: windows-sdk-content
description: Initializes sample protection on the downstream component.
old-location: mf\imfsampleprotection_initinputprotection.htm
tech.root: medfound
ms.assetid: 2bd43f33-8528-4e78-97d5-2af39a2ac06b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 2bd43f33-8528-4e78-97d5-2af39a2ac06b, IMFSampleProtection interface [Media Foundation],InitInputProtection method, IMFSampleProtection.InitInputProtection, IMFSampleProtection::InitInputProtection, InitInputProtection, InitInputProtection method [Media Foundation], InitInputProtection method [Media Foundation],IMFSampleProtection interface, mf.imfsampleprotection_initinputprotection, mfidl/IMFSampleProtection::InitInputProtection
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
 - IMFSampleProtection.InitInputProtection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSampleProtection::InitInputProtection


## -description



Initializes sample protection on the downstream component.




## -parameters




### -param dwVersion [in]

Specifies the version number of the sample protection scheme. The version number is specified as a <a href="https://msdn.microsoft.com/5244ac44-5738-4d77-9dc5-371efe52ced9">SAMPLE_PROTECTION_VERSION</a> enumeration value.


### -param dwInputId [in]

Identifier of the input stream. The identifier corresponds to the output stream identifier returned by the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface.


### -param pbSeed [in]

Pointer to a buffer that contains the initialization data provided by the upstream component. To retrieve this buffer, call <a href="https://msdn.microsoft.com/03bee13d-1c51-4b26-98bb-bac15264aa54">IMFSampleProtection::InitOutputProtection</a>.


### -param cbSeed [in]

Size of the <i>pbSeed</i> buffer, in bytes.


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
 




## -see-also




<a href="https://msdn.microsoft.com/bebe24cd-657b-4c6c-9fe9-5d6dd58827a3">IMFSampleProtection</a>
 

 


---
UID: NF:wmcontainer.IMFASFContentInfo.GetEncodingConfigurationPropertyStore
title: IMFASFContentInfo::GetEncodingConfigurationPropertyStore
author: windows-sdk-content
description: Retrieves a property store that can be used to set encoding properties.
old-location: mf\imfasfcontentinfo_getencodingconfigurationpropertystore.htm
tech.root: medfound
ms.assetid: e77a5564-82bc-4c1d-9fb8-84ab484c4ca8
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetEncodingConfigurationPropertyStore, GetEncodingConfigurationPropertyStore method [Media Foundation], GetEncodingConfigurationPropertyStore method [Media Foundation],IMFASFContentInfo interface, IMFASFContentInfo interface [Media Foundation],GetEncodingConfigurationPropertyStore method, IMFASFContentInfo.GetEncodingConfigurationPropertyStore, IMFASFContentInfo::GetEncodingConfigurationPropertyStore, e77a5564-82bc-4c1d-9fb8-84ab484c4ca8, mf.imfasfcontentinfo_getencodingconfigurationpropertystore, wmcontainer/IMFASFContentInfo::GetEncodingConfigurationPropertyStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
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
 - IMFASFContentInfo.GetEncodingConfigurationPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmcontainer.h
: 
- IMFASFContentInfo.GetEncodingConfigurationPropertyStore
: 
---

# IMFASFContentInfo::GetEncodingConfigurationPropertyStore


## -description



Retrieves a property store that can be used to set encoding properties.




## -parameters




### -param wStreamNumber [in]

Stream number to configure. Set to zero to configure file-level encoding properties.


### -param ppIStore [out]

Receives a pointer to the <b>IPropertyStore</b> interface. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo Object</a>



<a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a>



<a href="https://msdn.microsoft.com/30e3c10b-1310-4194-8b83-221dfe73b03c">Setting Properties in the ContentInfo Object</a>
 

 


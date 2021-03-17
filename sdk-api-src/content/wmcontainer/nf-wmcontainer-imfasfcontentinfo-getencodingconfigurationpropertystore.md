---
UID: NF:wmcontainer.IMFASFContentInfo.GetEncodingConfigurationPropertyStore
title: IMFASFContentInfo::GetEncodingConfigurationPropertyStore (wmcontainer.h)
description: Retrieves a property store that can be used to set encoding properties.
helpviewer_keywords: ["GetEncodingConfigurationPropertyStore","GetEncodingConfigurationPropertyStore method [Media Foundation]","GetEncodingConfigurationPropertyStore method [Media Foundation]","IMFASFContentInfo interface","IMFASFContentInfo interface [Media Foundation]","GetEncodingConfigurationPropertyStore method","IMFASFContentInfo.GetEncodingConfigurationPropertyStore","IMFASFContentInfo::GetEncodingConfigurationPropertyStore","e77a5564-82bc-4c1d-9fb8-84ab484c4ca8","mf.imfasfcontentinfo_getencodingconfigurationpropertystore","wmcontainer/IMFASFContentInfo::GetEncodingConfigurationPropertyStore"]
old-location: mf\imfasfcontentinfo_getencodingconfigurationpropertystore.htm
tech.root: mf
ms.assetid: e77a5564-82bc-4c1d-9fb8-84ab484c4ca8
ms.date: 12/05/2018
ms.keywords: GetEncodingConfigurationPropertyStore, GetEncodingConfigurationPropertyStore method [Media Foundation], GetEncodingConfigurationPropertyStore method [Media Foundation],IMFASFContentInfo interface, IMFASFContentInfo interface [Media Foundation],GetEncodingConfigurationPropertyStore method, IMFASFContentInfo.GetEncodingConfigurationPropertyStore, IMFASFContentInfo::GetEncodingConfigurationPropertyStore, e77a5564-82bc-4c1d-9fb8-84ab484c4ca8, mf.imfasfcontentinfo_getencodingconfigurationpropertystore, wmcontainer/IMFASFContentInfo::GetEncodingConfigurationPropertyStore
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFContentInfo::GetEncodingConfigurationPropertyStore
 - wmcontainer/IMFASFContentInfo::GetEncodingConfigurationPropertyStore
dev_langs:
 - c++
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

<a href="/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a>



<a href="/windows/desktop/medfound/setting-properties-in-the-contentinfo-object">Setting Properties in the ContentInfo Object</a>
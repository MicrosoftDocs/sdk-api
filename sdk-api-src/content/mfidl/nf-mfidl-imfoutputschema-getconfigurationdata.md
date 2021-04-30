---
UID: NF:mfidl.IMFOutputSchema.GetConfigurationData
title: IMFOutputSchema::GetConfigurationData (mfidl.h)
description: Returns configuration data for the output protection system. The configuration data is used to enable or disable the protection system, and to set the protection levels.
helpviewer_keywords: ["26730d2d-8ebc-441b-a262-db0c8fe7e75a","GetConfigurationData","GetConfigurationData method [Media Foundation]","GetConfigurationData method [Media Foundation]","IMFOutputSchema interface","IMFOutputSchema interface [Media Foundation]","GetConfigurationData method","IMFOutputSchema.GetConfigurationData","IMFOutputSchema::GetConfigurationData","mf.imfoutputschema_getconfigurationdata","mfidl/IMFOutputSchema::GetConfigurationData"]
old-location: mf\imfoutputschema_getconfigurationdata.htm
tech.root: mf
ms.assetid: 26730d2d-8ebc-441b-a262-db0c8fe7e75a
ms.date: 12/05/2018
ms.keywords: 26730d2d-8ebc-441b-a262-db0c8fe7e75a, GetConfigurationData, GetConfigurationData method [Media Foundation], GetConfigurationData method [Media Foundation],IMFOutputSchema interface, IMFOutputSchema interface [Media Foundation],GetConfigurationData method, IMFOutputSchema.GetConfigurationData, IMFOutputSchema::GetConfigurationData, mf.imfoutputschema_getconfigurationdata, mfidl/IMFOutputSchema::GetConfigurationData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFOutputSchema::GetConfigurationData
 - mfidl/IMFOutputSchema::GetConfigurationData
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
 - IMFOutputSchema.GetConfigurationData
---

# IMFOutputSchema::GetConfigurationData


## -description

Returns configuration data for the output protection system. The configuration data is used to enable or disable the protection system, and to set the protection levels.

## -parameters

### -param pdwVal [out]

Receives the configuration data. The meaning of this data depends on the output protection system.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema">IMFOutputSchema</a>
---
UID: NF:mfidl.IMFSensorGroup.GetSensorGroupAttributes
title: IMFSensorGroup::GetSensorGroupAttributes (mfidl.h)
description: Gets the IMFAttributes for the sensor group. The returned object is a live reference to the internal attribute store.
helpviewer_keywords: ["GetSensorGroupAttributes","GetSensorGroupAttributes method [Media Foundation]","GetSensorGroupAttributes method [Media Foundation]","IMFSensorGroup interface","IMFSensorGroup interface [Media Foundation]","GetSensorGroupAttributes method","IMFSensorGroup.GetSensorGroupAttributes","IMFSensorGroup::GetSensorGroupAttributes","mf.imfsensorgroup_getsensorgroupattributes","mfidl/IMFSensorGroup::GetSensorGroupAttributes"]
old-location: mf\imfsensorgroup_getsensorgroupattributes.htm
tech.root: mf
ms.assetid: 4EFC4615-AD97-4F58-9BEE-63F965DF8DDE
ms.date: 12/05/2018
ms.keywords: GetSensorGroupAttributes, GetSensorGroupAttributes method [Media Foundation], GetSensorGroupAttributes method [Media Foundation],IMFSensorGroup interface, IMFSensorGroup interface [Media Foundation],GetSensorGroupAttributes method, IMFSensorGroup.GetSensorGroupAttributes, IMFSensorGroup::GetSensorGroupAttributes, mf.imfsensorgroup_getsensorgroupattributes, mfidl/IMFSensorGroup::GetSensorGroupAttributes
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorGroup::GetSensorGroupAttributes
 - mfidl/IMFSensorGroup::GetSensorGroupAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorGroup.GetSensorGroupAttributes
---

# IMFSensorGroup::GetSensorGroupAttributes


## -description

Gets the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> for the sensor group. The returned object is a live reference to the internal attribute store.

## -parameters

### -param ppAttributes [out]

The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface representing the internal attribute store of the sensor group.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppAttributes</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The sensor group has not been initialized.

</td>
</tr>
</table>

## -remarks

The caller may optionally use this attribute store to query for attributes set on the sensor group or modify/add attributes to the sensor group.  Modification of this attribute set is not persisted and will only be valid for the instance of the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a>.


This attribute store can be used to add runtime attributes for the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> that can be created using the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-createmediasource">IMFSensorGroup::CreateMediaSource</a> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a>
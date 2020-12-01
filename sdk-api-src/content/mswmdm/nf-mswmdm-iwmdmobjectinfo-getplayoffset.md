---
UID: NF:mswmdm.IWMDMObjectInfo.GetPlayOffset
title: IWMDMObjectInfo::GetPlayOffset (mswmdm.h)
description: The GetPlayOffset method retrieves the play offset of the object, in units appropriate to the format. This is the starting point for the next invocation of Play.
helpviewer_keywords: ["GetPlayOffset","GetPlayOffset method [windows Media Device Manager]","GetPlayOffset method [windows Media Device Manager]","IWMDMObjectInfo interface","IWMDMObjectInfo interface [windows Media Device Manager]","GetPlayOffset method","IWMDMObjectInfo.GetPlayOffset","IWMDMObjectInfo::GetPlayOffset","IWMDMObjectInfoGetPlayOffset","mswmdm/IWMDMObjectInfo::GetPlayOffset","wmdm.iwmdmobjectinfo_getplayoffset"]
old-location: wmdm\iwmdmobjectinfo_getplayoffset.htm
tech.root: WMDM
ms.assetid: 8642404a-33ff-40b7-b05a-f193e8feadf5
ms.date: 12/05/2018
ms.keywords: GetPlayOffset, GetPlayOffset method [windows Media Device Manager], GetPlayOffset method [windows Media Device Manager],IWMDMObjectInfo interface, IWMDMObjectInfo interface [windows Media Device Manager],GetPlayOffset method, IWMDMObjectInfo.GetPlayOffset, IWMDMObjectInfo::GetPlayOffset, IWMDMObjectInfoGetPlayOffset, mswmdm/IWMDMObjectInfo::GetPlayOffset, wmdm.iwmdmobjectinfo_getplayoffset
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMObjectInfo::GetPlayOffset
 - mswmdm/IWMDMObjectInfo::GetPlayOffset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMObjectInfo.GetPlayOffset
---

# IWMDMObjectInfo::GetPlayOffset


## -description

The <b>GetPlayOffset</b> method retrieves the play offset of the object, in units appropriate to the format. This is the starting point for the next invocation of <b>Play</b>.

## -parameters

### -param pdwOffset [out]

Pointer to a <b>DWORD</b> specifying the play offset of the object, in units appropriate to the format.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The value retrieved is either zero (if the <b>SetPlayOffset</b> method has not been called) or the value set by <b>SetPlayOffset</b> clipped to be no greater than the total play length of the object minus one unit.

For playable files, the value returned is specified in milliseconds. The play offset value does not change when the user starts playing a file on the media device or when an application invokes the <b>IWMDMDeviceControl::Play</b> method.

For folders or file systems containing playable files, the value returned indicates the first track that is played when an application invokes the <b>IWMDMDeviceControl::Play</b> method.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-play">Play</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-setplayoffset">SetPlayOffset</a>
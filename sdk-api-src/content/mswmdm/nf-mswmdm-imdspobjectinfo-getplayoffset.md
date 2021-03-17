---
UID: NF:mswmdm.IMDSPObjectInfo.GetPlayOffset
title: IMDSPObjectInfo::GetPlayOffset (mswmdm.h)
description: The GetPlayOffset method retrieves the play offset of the object, in units pertinent to the object. This is the starting point for the next invocation of IMDSPDeviceControl::Play.
helpviewer_keywords: ["GetPlayOffset","GetPlayOffset method [windows Media Device Manager]","GetPlayOffset method [windows Media Device Manager]","IMDSPObjectInfo interface","IMDSPObjectInfo interface [windows Media Device Manager]","GetPlayOffset method","IMDSPObjectInfo.GetPlayOffset","IMDSPObjectInfo::GetPlayOffset","IMDSPObjectInfoGetPlayOffset","mswmdm/IMDSPObjectInfo::GetPlayOffset","wmdm.imdspobjectinfo_getplayoffset"]
old-location: wmdm\imdspobjectinfo_getplayoffset.htm
tech.root: WMDM
ms.assetid: 3e801b95-aa44-4275-8a21-f68fbf6240f1
ms.date: 12/05/2018
ms.keywords: GetPlayOffset, GetPlayOffset method [windows Media Device Manager], GetPlayOffset method [windows Media Device Manager],IMDSPObjectInfo interface, IMDSPObjectInfo interface [windows Media Device Manager],GetPlayOffset method, IMDSPObjectInfo.GetPlayOffset, IMDSPObjectInfo::GetPlayOffset, IMDSPObjectInfoGetPlayOffset, mswmdm/IMDSPObjectInfo::GetPlayOffset, wmdm.imdspobjectinfo_getplayoffset
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
 - IMDSPObjectInfo::GetPlayOffset
 - mswmdm/IMDSPObjectInfo::GetPlayOffset
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
 - IMDSPObjectInfo.GetPlayOffset
---

# IMDSPObjectInfo::GetPlayOffset


## -description

The <b>GetPlayOffset</b> method retrieves the play offset of the object, in units pertinent to the object. This is the starting point for the next invocation of <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-play">IMDSPDeviceControl::Play</a>.

## -parameters

### -param pdwOffset [out]

Pointer to a <b>DWORD</b> containing the play offset of the object, in units pertinent to the object.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The value retrieved is either zero (if the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-setplayoffset">SetPlayOffset</a> method has not been called) or the value set by <b>SetPlayOffset</b> clipped to be no greater than the total play length of the object minus one unit.

For playable files, the value returned is specified in milliseconds. The play offset value does not change when the user starts playing a file on the media device or when an application invokes the <b>IMDSPDeviceControl::Play</b> method.

For folders or file systems containing playable files, the value returned indicates the first track that is played when an application invokes the <b>IMDSPDeviceControl::Play</b> method.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo">IMDSPObjectInfo Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-setplayoffset">IMDSPObjectInfo::SetPlayOffset</a>
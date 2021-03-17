---
UID: NF:mswmdm.IMDSPObjectInfo.SetPlayOffset
title: IMDSPObjectInfo::SetPlayOffset (mswmdm.h)
description: The SetPlayOffset method sets the play offset of the object, in the units pertinent to the object. This specifies the starting point for the next invocation of IMDSPDeviceControl::Play.
helpviewer_keywords: ["IMDSPObjectInfo interface [windows Media Device Manager]","SetPlayOffset method","IMDSPObjectInfo.SetPlayOffset","IMDSPObjectInfo::SetPlayOffset","IMDSPObjectInfoSetPlayOffset","SetPlayOffset","SetPlayOffset method [windows Media Device Manager]","SetPlayOffset method [windows Media Device Manager]","IMDSPObjectInfo interface","mswmdm/IMDSPObjectInfo::SetPlayOffset","wmdm.imdspobjectinfo_setplayoffset"]
old-location: wmdm\imdspobjectinfo_setplayoffset.htm
tech.root: WMDM
ms.assetid: f61ce3b5-3cd9-41e6-9a29-42b9832ec55a
ms.date: 12/05/2018
ms.keywords: IMDSPObjectInfo interface [windows Media Device Manager],SetPlayOffset method, IMDSPObjectInfo.SetPlayOffset, IMDSPObjectInfo::SetPlayOffset, IMDSPObjectInfoSetPlayOffset, SetPlayOffset, SetPlayOffset method [windows Media Device Manager], SetPlayOffset method [windows Media Device Manager],IMDSPObjectInfo interface, mswmdm/IMDSPObjectInfo::SetPlayOffset, wmdm.imdspobjectinfo_setplayoffset
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
 - IMDSPObjectInfo::SetPlayOffset
 - mswmdm/IMDSPObjectInfo::SetPlayOffset
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
 - IMDSPObjectInfo.SetPlayOffset
---

# IMDSPObjectInfo::SetPlayOffset


## -description

The <b>SetPlayOffset</b> method sets the play offset of the object, in the units pertinent to the object. This specifies the starting point for the next invocation of <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-play">IMDSPDeviceControl::Play</a>.

## -parameters

### -param dwOffset [in]

<b>DWORD</b> containing the play offset to set for the object, in units pertinent to the object.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

If the value passed is greater than the total length of the object minus the current play length, it is clipped to the length of the object minus the play length.

For playable files, the value is specified in milliseconds. The play offset position value does not change when the user starts playing a file on the media device or when an application invokes the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-play">IMDSPDeviceControl::Play</a> method.

For folders or file systems containing playable files, the value indicates the first track that is played when an application invokes the <b>IMDSPDeviceControl::Play</b> method.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo">IMDSPObjectInfo Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-getplayoffset">IMDSPObjectInfo::GetPlayOffset</a>
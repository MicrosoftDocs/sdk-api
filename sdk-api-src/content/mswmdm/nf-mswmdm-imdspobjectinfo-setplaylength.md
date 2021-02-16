---
UID: NF:mswmdm.IMDSPObjectInfo.SetPlayLength
title: IMDSPObjectInfo::SetPlayLength (mswmdm.h)
description: The SetPlayLength method sets the play length of the object, in units pertinent to the object. This is the maximum length that the object plays regardless of its actual length.
helpviewer_keywords: ["IMDSPObjectInfo interface [windows Media Device Manager]","SetPlayLength method","IMDSPObjectInfo.SetPlayLength","IMDSPObjectInfo::SetPlayLength","IMDSPObjectInfoSetPlayLength","SetPlayLength","SetPlayLength method [windows Media Device Manager]","SetPlayLength method [windows Media Device Manager]","IMDSPObjectInfo interface","mswmdm/IMDSPObjectInfo::SetPlayLength","wmdm.imdspobjectinfo_setplaylength"]
old-location: wmdm\imdspobjectinfo_setplaylength.htm
tech.root: WMDM
ms.assetid: d5d860fb-c146-4bfc-90b1-cf1dfc81c5ba
ms.date: 12/05/2018
ms.keywords: IMDSPObjectInfo interface [windows Media Device Manager],SetPlayLength method, IMDSPObjectInfo.SetPlayLength, IMDSPObjectInfo::SetPlayLength, IMDSPObjectInfoSetPlayLength, SetPlayLength, SetPlayLength method [windows Media Device Manager], SetPlayLength method [windows Media Device Manager],IMDSPObjectInfo interface, mswmdm/IMDSPObjectInfo::SetPlayLength, wmdm.imdspobjectinfo_setplaylength
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
 - IMDSPObjectInfo::SetPlayLength
 - mswmdm/IMDSPObjectInfo::SetPlayLength
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
 - IMDSPObjectInfo.SetPlayLength
---

# IMDSPObjectInfo::SetPlayLength


## -description

The <b>SetPlayLength</b> method sets the play length of the object, in units pertinent to the object. This is the maximum length that the object plays regardless of its actual length.

## -parameters

### -param dwLength [in]

<b>DWORD</b> containing the play length to set for the object, in units pertinent to the object.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

If the value passed in is greater than the total length of the object, it is clipped to the length of the object minus the object's current play position minus one unit.

For playable files, the value to set is specified in milliseconds. The value is clipped to no more than the total length of the file minus the object's current play offset position. The play position information can change either when the user starts playing a file on the media device or when an application invokes the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-play">IMDSPDeviceControl::Play</a> method.

For folders or file systems containing playable files, the value passed is the number of playable files in that folder or in the root of that file system.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo">IMDSPObjectInfo Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-getplaylength">IMDSPObjectInfo::GetPlayLength</a>
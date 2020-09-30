---
UID: NF:mswmdm.IMDSPObjectInfo.GetPlayLength
title: IMDSPObjectInfo::GetPlayLength (mswmdm.h)
description: The GetPlayLength method retrieves the play length of the object in units pertinent to the object. This is the remaining length that the object can play, not its total length.
helpviewer_keywords: ["GetPlayLength","GetPlayLength method [windows Media Device Manager]","GetPlayLength method [windows Media Device Manager]","IMDSPObjectInfo interface","IMDSPObjectInfo interface [windows Media Device Manager]","GetPlayLength method","IMDSPObjectInfo.GetPlayLength","IMDSPObjectInfo::GetPlayLength","IMDSPObjectInfoGetPlayLength","mswmdm/IMDSPObjectInfo::GetPlayLength","wmdm.imdspobjectinfo_getplaylength"]
old-location: wmdm\imdspobjectinfo_getplaylength.htm
tech.root: WMDM
ms.assetid: d5f2188f-f813-4c42-9878-52836ec8ebdc
ms.date: 12/05/2018
ms.keywords: GetPlayLength, GetPlayLength method [windows Media Device Manager], GetPlayLength method [windows Media Device Manager],IMDSPObjectInfo interface, IMDSPObjectInfo interface [windows Media Device Manager],GetPlayLength method, IMDSPObjectInfo.GetPlayLength, IMDSPObjectInfo::GetPlayLength, IMDSPObjectInfoGetPlayLength, mswmdm/IMDSPObjectInfo::GetPlayLength, wmdm.imdspobjectinfo_getplaylength
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
 - IMDSPObjectInfo::GetPlayLength
 - mswmdm/IMDSPObjectInfo::GetPlayLength
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
 - IMDSPObjectInfo.GetPlayLength
---

# IMDSPObjectInfo::GetPlayLength


## -description

The <b>GetPlayLength</b> method retrieves the play length of the object in units pertinent to the object. This is the remaining length that the object can play, not its total length.

## -parameters

### -param pdwLength [out]

Pointer to a <b>DWORD</b> containing the remaining play length of the object.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The value of the play length retrieved is either the total length of the object minus the current play position (if the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-setplaylength">IMDSPObjectInfo::SetPlayLength</a> method has not been called), or the value set by <b>IMDSPObjectInfo::SetPlayLength</b> clipped to be no greater than the total play length of the object minus the current play position.

For playable files, the value returned is specified in milliseconds. The play length information can change either when the user starts playing a file on the media device or when an application invokes the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevicecontrol-play">IMDSPDeviceControl::Play</a> method.

For folders or file systems containing playable files, the value returned is in tracks or numbers of playable files in that folder or in the root of that file system.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo">IMDSPObjectInfo Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-setplaylength">IMDSPObjectInfo::SetPlayLength</a>
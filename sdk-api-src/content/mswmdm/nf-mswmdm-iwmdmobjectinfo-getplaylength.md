---
UID: NF:mswmdm.IWMDMObjectInfo.GetPlayLength
title: IWMDMObjectInfo::GetPlayLength (mswmdm.h)
description: The GetPlayLength method retrieves the play length of the object in units appropriate to the format. This is the remaining length that the file can play, not its total length.
helpviewer_keywords: ["GetPlayLength","GetPlayLength method [windows Media Device Manager]","GetPlayLength method [windows Media Device Manager]","IWMDMObjectInfo interface","IWMDMObjectInfo interface [windows Media Device Manager]","GetPlayLength method","IWMDMObjectInfo.GetPlayLength","IWMDMObjectInfo::GetPlayLength","IWMDMObjectInfoGetPlayLength","mswmdm/IWMDMObjectInfo::GetPlayLength","wmdm.iwmdmobjectinfo_getplaylength"]
old-location: wmdm\iwmdmobjectinfo_getplaylength.htm
tech.root: WMDM
ms.assetid: 7f553513-0928-41b8-858f-c06ec57660d1
ms.date: 12/05/2018
ms.keywords: GetPlayLength, GetPlayLength method [windows Media Device Manager], GetPlayLength method [windows Media Device Manager],IWMDMObjectInfo interface, IWMDMObjectInfo interface [windows Media Device Manager],GetPlayLength method, IWMDMObjectInfo.GetPlayLength, IWMDMObjectInfo::GetPlayLength, IWMDMObjectInfoGetPlayLength, mswmdm/IWMDMObjectInfo::GetPlayLength, wmdm.iwmdmobjectinfo_getplaylength
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
 - IWMDMObjectInfo::GetPlayLength
 - mswmdm/IWMDMObjectInfo::GetPlayLength
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
 - IWMDMObjectInfo.GetPlayLength
---

# IWMDMObjectInfo::GetPlayLength


## -description

The <b>GetPlayLength</b> method retrieves the play length of the object in units appropriate to the format. This is the remaining length that the file can play, not its total length.

## -parameters

### -param pdwLength [out]

Pointer to a <b>DWORD</b> specifying the remaining play length of the file, in milliseconds.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The value of the play length retrieved is either the total length of the object minus the current play position (if the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-setplaylength">SetPlayLength</a> method has not been called), or the value set by <b>SetPlayLength</b> clipped to be no greater than the total play length of the object minus the current play position.

The play length information can change either when the user starts playing a file on the media device or when an application invokes the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-play">Play</a> method.

For folders or file systems containing playable files, the value returned is in tracks or numbers of playable files in that folder or in the root of that file system.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-play">Play</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-setplaylength">SetPlayLength</a>
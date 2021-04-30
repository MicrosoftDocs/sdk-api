---
UID: NF:mswmdm.IWMDMStorage4.GetRightsWithProgress
title: IWMDMStorage4::GetRightsWithProgress (mswmdm.h)
description: The GetRightsWithProgress method retrieves the rights information for the storage object, providing a callback mechanism for monitoring progress.
helpviewer_keywords: ["GetRightsWithProgress","GetRightsWithProgress method [windows Media Device Manager]","GetRightsWithProgress method [windows Media Device Manager]","IWMDMStorage4 interface","IWMDMStorage4 interface [windows Media Device Manager]","GetRightsWithProgress method","IWMDMStorage4.GetRightsWithProgress","IWMDMStorage4::GetRightsWithProgress","IWMDMStorage4GetRightsWithProgress","mswmdm/IWMDMStorage4::GetRightsWithProgress","wmdm.iwmdmstorage4_getrightswithprogress"]
old-location: wmdm\iwmdmstorage4_getrightswithprogress.htm
tech.root: WMDM
ms.assetid: 63df4448-75f0-4152-a308-15f6f10e8564
ms.date: 12/05/2018
ms.keywords: GetRightsWithProgress, GetRightsWithProgress method [windows Media Device Manager], GetRightsWithProgress method [windows Media Device Manager],IWMDMStorage4 interface, IWMDMStorage4 interface [windows Media Device Manager],GetRightsWithProgress method, IWMDMStorage4.GetRightsWithProgress, IWMDMStorage4::GetRightsWithProgress, IWMDMStorage4GetRightsWithProgress, mswmdm/IWMDMStorage4::GetRightsWithProgress, wmdm.iwmdmstorage4_getrightswithprogress
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
 - IWMDMStorage4::GetRightsWithProgress
 - mswmdm/IWMDMStorage4::GetRightsWithProgress
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
 - IWMDMStorage4.GetRightsWithProgress
---

# IWMDMStorage4::GetRightsWithProgress


## -description

The <b>GetRightsWithProgress</b> method retrieves the rights information for the storage object, providing a callback mechanism for monitoring progress.

## -parameters

### -param pIProgressCallback [in]

Optional pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3</a> interface to be used by Windows Media Device Manager to report progress back to the application.

### -param ppRights [out]

Pointer to an array of <a href="/windows/desktop/WMDM/wmdmrights">WMDMRIGHTS</a> structures that contain the storage object rights information. Memory for this array is allocated by Windows Media Device Manager. When the calling application has finished accessing this array, the memory must be freed by using <b>CoTaskMemFree</b>.

### -param pnRightsCount [out]

Pointer to the number of <b>WMDMRIGHTS</b> structures in the <i>ppRights</i> array.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Object rights describe the usage permissions for digital media content. For example, the <b>WMDMRIGHTS</b> structure can contain information concerning how many times a file can be played and who can play it.

Retrieving rights from a licensed file can sometimes be a lengthy request; this function allows a rights request to be performed asynchronously.

The secure content provider can generate event notifications on the callback <i>pIProgressCallback</i> in addition to the progress notifications. Examples of such events include acquiring a secure clock, initializing DRM, and so on. These events are described in <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-progress3">IWMDMProgress3::Progress3</a>.

This method is identical to <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights">IWMDMStorage::GetRights</a>, except it returns progress, and does not provide a MAC for parameter verification.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4">IWMDMStorage4 Interface</a>
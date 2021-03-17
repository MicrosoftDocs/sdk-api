---
UID: NF:mswmdm.IWMDMObjectInfo.GetTotalLength
title: IWMDMObjectInfo::GetTotalLength (mswmdm.h)
description: The GetTotalLength method retrieves the total play length of the object, in units appropriate to the format. The value returned is the total length regardless of the current settings of the play length and offset.
helpviewer_keywords: ["GetTotalLength","GetTotalLength method [windows Media Device Manager]","GetTotalLength method [windows Media Device Manager]","IWMDMObjectInfo interface","IWMDMObjectInfo interface [windows Media Device Manager]","GetTotalLength method","IWMDMObjectInfo.GetTotalLength","IWMDMObjectInfo::GetTotalLength","IWMDMObjectInfoGetTotalLength","mswmdm/IWMDMObjectInfo::GetTotalLength","wmdm.iwmdmobjectinfo_gettotallength"]
old-location: wmdm\iwmdmobjectinfo_gettotallength.htm
tech.root: WMDM
ms.assetid: ca0e0efc-ff2e-40d6-ace3-5644013bccff
ms.date: 12/05/2018
ms.keywords: GetTotalLength, GetTotalLength method [windows Media Device Manager], GetTotalLength method [windows Media Device Manager],IWMDMObjectInfo interface, IWMDMObjectInfo interface [windows Media Device Manager],GetTotalLength method, IWMDMObjectInfo.GetTotalLength, IWMDMObjectInfo::GetTotalLength, IWMDMObjectInfoGetTotalLength, mswmdm/IWMDMObjectInfo::GetTotalLength, wmdm.iwmdmobjectinfo_gettotallength
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
 - IWMDMObjectInfo::GetTotalLength
 - mswmdm/IWMDMObjectInfo::GetTotalLength
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
 - IWMDMObjectInfo.GetTotalLength
---

# IWMDMObjectInfo::GetTotalLength


## -description

The <b>GetTotalLength</b> method retrieves the total play length of the object, in units appropriate to the format. The value returned is the total length regardless of the current settings of the play length and offset.

## -parameters

### -param pdwLength [out]

Pointer to a <b>DWORD</b> specifying the total length of the file, in units appropriate to the format.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

For playable files, the total length is specified in milliseconds.

For folders or file systems containing playable files, the value returned indicates the total number of playable files in a folder or in the root of a file system.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>
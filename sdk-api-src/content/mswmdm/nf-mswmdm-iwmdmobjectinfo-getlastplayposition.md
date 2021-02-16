---
UID: NF:mswmdm.IWMDMObjectInfo.GetLastPlayPosition
title: IWMDMObjectInfo::GetLastPlayPosition (mswmdm.h)
description: The GetLastPlayPosition method retrieves the last play position of the object. The object must be an audio file on the media device.
helpviewer_keywords: ["GetLastPlayPosition","GetLastPlayPosition method [windows Media Device Manager]","GetLastPlayPosition method [windows Media Device Manager]","IWMDMObjectInfo interface","IWMDMObjectInfo interface [windows Media Device Manager]","GetLastPlayPosition method","IWMDMObjectInfo.GetLastPlayPosition","IWMDMObjectInfo::GetLastPlayPosition","IWMDMObjectInfoGetLastPlayPosition","mswmdm/IWMDMObjectInfo::GetLastPlayPosition","wmdm.iwmdmobjectinfo_getlastplayposition"]
old-location: wmdm\iwmdmobjectinfo_getlastplayposition.htm
tech.root: WMDM
ms.assetid: d5b5cf7c-6969-497e-bf2c-e91ddb85f701
ms.date: 12/05/2018
ms.keywords: GetLastPlayPosition, GetLastPlayPosition method [windows Media Device Manager], GetLastPlayPosition method [windows Media Device Manager],IWMDMObjectInfo interface, IWMDMObjectInfo interface [windows Media Device Manager],GetLastPlayPosition method, IWMDMObjectInfo.GetLastPlayPosition, IWMDMObjectInfo::GetLastPlayPosition, IWMDMObjectInfoGetLastPlayPosition, mswmdm/IWMDMObjectInfo::GetLastPlayPosition, wmdm.iwmdmobjectinfo_getlastplayposition
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
 - IWMDMObjectInfo::GetLastPlayPosition
 - mswmdm/IWMDMObjectInfo::GetLastPlayPosition
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
 - IWMDMObjectInfo.GetLastPlayPosition
---

# IWMDMObjectInfo::GetLastPlayPosition


## -description

The <b>GetLastPlayPosition</b> method retrieves the last play position of the object. The object must be an audio file on the media device.

## -parameters

### -param pdwLastPos [out]

Pointer to a <b>DWORD</b> specifying the last play position of the object, in milliseconds.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The object must be an audio data file. For all other object types, this function returns E_INVALIDTYPE.

The last play position changes when either the user starts playing a file on the media device or when an application invokes the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-play">IWMDMDeviceControl::Play</a> method.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-play">Play</a>
---
UID: NF:windowsstoragecom.IRandomAccessStreamFileAccessMode.GetMode
title: IRandomAccessStreamFileAccessMode::GetMode (windowsstoragecom.h)
description: Retrieves the file access mode that was used when the StorageFile.OpenAsync method was called to open the random-access byte stream.
helpviewer_keywords: ["GetMode","GetMode method [Windows Runtime]","GetMode method [Windows Runtime]","IRandomAccessStreamFileAccessMode interface","IRandomAccessStreamFileAccessMode interface [Windows Runtime]","GetMode method","IRandomAccessStreamFileAccessMode.GetMode","IRandomAccessStreamFileAccessMode::GetMode","windowsstoragecom/IRandomAccessStreamFileAccessMode::GetMode","winrt.irandomaccessstreamfileaccessmode_getmode"]
old-location: winrt\irandomaccessstreamfileaccessmode_getmode.htm
tech.root: WinRT
ms.assetid: F542C4E4-5B65-4909-AF08-C129297A1085
ms.date: 12/05/2018
ms.keywords: GetMode, GetMode method [Windows Runtime], GetMode method [Windows Runtime],IRandomAccessStreamFileAccessMode interface, IRandomAccessStreamFileAccessMode interface [Windows Runtime],GetMode method, IRandomAccessStreamFileAccessMode.GetMode, IRandomAccessStreamFileAccessMode::GetMode, windowsstoragecom/IRandomAccessStreamFileAccessMode::GetMode, winrt.irandomaccessstreamfileaccessmode_getmode
req.header: windowsstoragecom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Windows.storage.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRandomAccessStreamFileAccessMode::GetMode
 - windowsstoragecom/IRandomAccessStreamFileAccessMode::GetMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.storage.dll
api_name:
 - IRandomAccessStreamFileAccessMode.GetMode
---

# IRandomAccessStreamFileAccessMode::GetMode


## -description

Retrieves the file access mode that was used when the <a href="/uwp/api/windows.storage.storagefile.openasync">StorageFile.OpenAsync</a> method was called to open the random-access byte stream.

## -parameters

### -param fileAccessMode [out]

The file access mode that was used when the <a href="/uwp/api/windows.storage.storagefile.openasync">StorageFile.OpenAsync</a> method was called to open the random-access byte stream. Cast this value as a <a href="/uwp/api/Windows.Storage.FileAccessMode">Windows::Storage::FileAccessMode</a> enumeration value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-irandomaccessstreamfileaccessmode">IRandomAccessStreamFileAccessMode</a>



<a href="/uwp/api/windows.storage.storagefile.openasync">StorageFile.OpenAsync</a>



<a href="/uwp/api/Windows.Storage.FileAccessMode">Windows::Storage::FileAccessMode</a>
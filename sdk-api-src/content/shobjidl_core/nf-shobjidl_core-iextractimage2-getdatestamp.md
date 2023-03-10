---
UID: NF:shobjidl_core.IExtractImage2.GetDateStamp
title: IExtractImage2::GetDateStamp (shobjidl_core.h)
description: Requests the date the image was last modified. This method allows the Shell to determine whether cached images are out-of-date.
helpviewer_keywords: ["GetDateStamp","GetDateStamp method [Windows Shell]","GetDateStamp method [Windows Shell]","IExtractImage2 interface","IExtractImage2 interface [Windows Shell]","GetDateStamp method","IExtractImage2.GetDateStamp","IExtractImage2::GetDateStamp","_win32_IExtractImage2_GetDateStamp","shell.IExtractImage2_GetDateStamp","shobjidl_core/IExtractImage2::GetDateStamp"]
old-location: shell\IExtractImage2_GetDateStamp.htm
tech.root: shell
ms.assetid: dca5fe16-bf83-4426-af2a-9a205f4ebd57
ms.date: 12/05/2018
ms.keywords: GetDateStamp, GetDateStamp method [Windows Shell], GetDateStamp method [Windows Shell],IExtractImage2 interface, IExtractImage2 interface [Windows Shell],GetDateStamp method, IExtractImage2.GetDateStamp, IExtractImage2::GetDateStamp, _win32_IExtractImage2_GetDateStamp, shell.IExtractImage2_GetDateStamp, shobjidl_core/IExtractImage2::GetDateStamp
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtractImage2::GetDateStamp
 - shobjidl_core/IExtractImage2::GetDateStamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IExtractImage2.GetDateStamp
---

# IExtractImage2::GetDateStamp


## -description

Requests the date the image was last modified. This method allows the Shell to determine whether cached images are out-of-date.

## -parameters

### -param pDateStamp

Type: <b>FILETIME*</b>

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure used to return the last time the image was modified.

## -returns

Type: <b>HRESULT</b>

Return S_OK if successful, or a COM-defined error code otherwise.
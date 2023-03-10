---
UID: NF:shobjidl.ICDBurn.Burn
title: ICDBurn::Burn (shobjidl.h)
description: Instructs data to be copied from the staging area to a writable CD.
helpviewer_keywords: ["Burn","Burn method [Windows Shell]","Burn method [Windows Shell]","ICDBurn interface","ICDBurn interface [Windows Shell]","Burn method","ICDBurn.Burn","ICDBurn::Burn","_shell_ICDBurn_Burn","shell.ICDBurn_Burn","shobjidl/ICDBurn::Burn"]
old-location: shell\ICDBurn_Burn.htm
tech.root: shell
ms.assetid: e081973a-e923-45de-93ba-3281be73cc93
ms.date: 12/05/2018
ms.keywords: Burn, Burn method [Windows Shell], Burn method [Windows Shell],ICDBurn interface, ICDBurn interface [Windows Shell],Burn method, ICDBurn.Burn, ICDBurn::Burn, _shell_ICDBurn_Burn, shell.ICDBurn_Burn, shobjidl/ICDBurn::Burn
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICDBurn::Burn
 - shobjidl/ICDBurn::Burn
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
 - ICDBurn.Burn
---

# ICDBurn::Burn


## -description

Instructs data to be copied from the staging area to a writable CD.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window of the UI.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>staging area</i> has a default location of %userprofile%\Local Settings\Application Data\Microsoft\CD Burning. Its actual path can be retrieved through <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a>, <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha">SHGetSpecialFolderPath</a>, <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation">SHGetFolderLocation</a>, <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation">SHGetSpecialFolderLocation</a>, or <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpathandsubdira">SHGetFolderPathAndSubDir</a> by using the CSIDL_CDBURN_AREA value.
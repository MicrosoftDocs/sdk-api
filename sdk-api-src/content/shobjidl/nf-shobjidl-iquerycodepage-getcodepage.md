---
UID: NF:shobjidl.IQueryCodePage.GetCodePage
title: IQueryCodePage::GetCodePage (shobjidl.h)
description: Retrieves the numeric value (Code Page identifier) of the ANSI code page.
helpviewer_keywords: ["GetCodePage","GetCodePage method [Windows Shell]","GetCodePage method [Windows Shell]","IQueryCodePage interface","IQueryCodePage interface [Windows Shell]","GetCodePage method","IQueryCodePage.GetCodePage","IQueryCodePage::GetCodePage","_shell_IQueryCodePage_GetCodePage","shell.IQueryCodePage_GetCodePage","shobjidl/IQueryCodePage::GetCodePage"]
old-location: shell\IQueryCodePage_GetCodePage.htm
tech.root: shell
ms.assetid: 05644051-c64e-443c-bc98-ed296bc0b8d9
ms.date: 12/05/2018
ms.keywords: GetCodePage, GetCodePage method [Windows Shell], GetCodePage method [Windows Shell],IQueryCodePage interface, IQueryCodePage interface [Windows Shell],GetCodePage method, IQueryCodePage.GetCodePage, IQueryCodePage::GetCodePage, _shell_IQueryCodePage_GetCodePage, shell.IQueryCodePage_GetCodePage, shobjidl/IQueryCodePage::GetCodePage
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryCodePage::GetCodePage
 - shobjidl/IQueryCodePage::GetCodePage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IQueryCodePage.GetCodePage
---

# IQueryCodePage::GetCodePage


## -description

Retrieves the numeric value (Code Page identifier) of the ANSI code page.

## -parameters

### -param puiCodePage [out]

Type: <b>UINT*</b>

The numeric value (Code Page identifier) of the ANSI code page.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


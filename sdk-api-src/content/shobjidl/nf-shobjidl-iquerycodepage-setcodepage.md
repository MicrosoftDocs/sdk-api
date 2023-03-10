---
UID: NF:shobjidl.IQueryCodePage.SetCodePage
title: IQueryCodePage::SetCodePage (shobjidl.h)
description: Sets the numeric value of the ANSI code page to a specified code page identifier.
helpviewer_keywords: ["IQueryCodePage interface [Windows Shell]","SetCodePage method","IQueryCodePage.SetCodePage","IQueryCodePage::SetCodePage","SetCodePage","SetCodePage method [Windows Shell]","SetCodePage method [Windows Shell]","IQueryCodePage interface","_shell_IQueryCodePage_SetCodePage","shell.IQueryCodePage_SetCodePage","shobjidl/IQueryCodePage::SetCodePage"]
old-location: shell\IQueryCodePage_SetCodePage.htm
tech.root: shell
ms.assetid: 19b9d796-e5a7-4b82-a299-95ee912db010
ms.date: 12/05/2018
ms.keywords: IQueryCodePage interface [Windows Shell],SetCodePage method, IQueryCodePage.SetCodePage, IQueryCodePage::SetCodePage, SetCodePage, SetCodePage method [Windows Shell], SetCodePage method [Windows Shell],IQueryCodePage interface, _shell_IQueryCodePage_SetCodePage, shell.IQueryCodePage_SetCodePage, shobjidl/IQueryCodePage::SetCodePage
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
 - IQueryCodePage::SetCodePage
 - shobjidl/IQueryCodePage::SetCodePage
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
 - IQueryCodePage.SetCodePage
---

# IQueryCodePage::SetCodePage


## -description

Sets the numeric value of the ANSI code page to a specified code page identifier.

## -parameters

### -param uiCodePage [in]

Type: <b>UINT</b>

The numeric value of the ANSI code page you want to set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


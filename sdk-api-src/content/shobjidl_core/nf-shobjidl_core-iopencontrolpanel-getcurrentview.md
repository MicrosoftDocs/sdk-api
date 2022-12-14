---
UID: NF:shobjidl_core.IOpenControlPanel.GetCurrentView
title: IOpenControlPanel::GetCurrentView (shobjidl_core.h)
description: Gets the most recent Control Panel view:\_Classic view or Category view.
helpviewer_keywords: ["CPVIEW_ALLITEMS","CPVIEW_CATEGORY","CPVIEW_CLASSIC","CPVIEW_HOME","GetCurrentView","GetCurrentView method [Windows Shell]","GetCurrentView method [Windows Shell]","IOpenControlPanel interface","IOpenControlPanel interface [Windows Shell]","GetCurrentView method","IOpenControlPanel.GetCurrentView","IOpenControlPanel::GetCurrentView","_shell_IOpenControlPanel_GetCurrentView","shell.IOpenControlPanel_GetCurrentView","shobjidl_core/IOpenControlPanel::GetCurrentView"]
old-location: shell\IOpenControlPanel_GetCurrentView.htm
tech.root: shell
ms.assetid: ed539638-7953-471f-ac90-ebd4c3929e8e
ms.date: 12/05/2018
ms.keywords: CPVIEW_ALLITEMS, CPVIEW_CATEGORY, CPVIEW_CLASSIC, CPVIEW_HOME, GetCurrentView, GetCurrentView method [Windows Shell], GetCurrentView method [Windows Shell],IOpenControlPanel interface, IOpenControlPanel interface [Windows Shell],GetCurrentView method, IOpenControlPanel.GetCurrentView, IOpenControlPanel::GetCurrentView, _shell_IOpenControlPanel_GetCurrentView, shell.IOpenControlPanel_GetCurrentView, shobjidl_core/IOpenControlPanel::GetCurrentView
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IOpenControlPanel::GetCurrentView
 - shobjidl_core/IOpenControlPanel::GetCurrentView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOpenControlPanel.GetCurrentView
---

# IOpenControlPanel::GetCurrentView


## -description

Gets the most recent Control Panel view: Classic view or Category view.

## -parameters

### -param pView [out]

Type: <b>CPVIEW*</b>

A pointer that receives the most recent view. Valid values are as follows:



#### CPVIEW_CLASSIC (0x0)

0x0. Classic view.



#### CPVIEW_ALLITEMS (CPVIEW_CLASSIC)

0x0. <b>Windows 7 and later</b>. Equivalent to CPVIEW_CLASSIC.



#### CPVIEW_CATEGORY (0x1)

0x1. Category view.



#### CPVIEW_HOME (0x1)

0x1. <b>Windows 7 and later</b>. Equivalent to CPVIEW_CATEGORY.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


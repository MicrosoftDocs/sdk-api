---
UID: NE:uiribbon.UI_OWNERSHIP
title: UI_OWNERSHIP
author: windows-sdk-content
description: Specifies values that identify the ownership conditions under which an image is created by the Windows Ribbon framework.
old-location: windowsribbon\windowsribbon_ui_ownership.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_ownership.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: UI_OWNERSHIP, UI_OWNERSHIP enumeration [Windows Ribbon], UI_OWNERSHIP_COPY, UI_OWNERSHIP_TRANSFER, scenicintent_UI_OWNERSHIP, uiribbon/UI_OWNERSHIP, uiribbon/UI_OWNERSHIP_COPY, uiribbon/UI_OWNERSHIP_TRANSFER, windowsribbon.windowsribbon_ui_ownership
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: uiribbon.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_OWNERSHIP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_OWNERSHIP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UI_OWNERSHIP enumeration


## -description


Specifies values that identify the ownership conditions under which an image is created by the Windows Ribbon framework.


## -enum-fields




### -field UI_OWNERSHIP_TRANSFER

The handle to the bitmap (HBITMAP) is owned by the Ribbon framework 
			through the <a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a> object.
			


### -field UI_OWNERSHIP_COPY

A copy of the HBITMAP is created by the Ribbon framework through 
			the <a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a> object. The host application still owns the HBITMAP.
			


## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/09eea6ad-c756-4044-b98f-6d6ba87437db">IUIImageFromBitmap::CreateImage</a>
 

 


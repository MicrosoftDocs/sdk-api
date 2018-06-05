---
UID: NF:oleauto.RevokeActiveObject
title: RevokeActiveObject function
author: windows-sdk-content
description: Ends an object's status as active.
old-location: automat\revokeactiveobject.htm
old-project: automat
ms.assetid: 47e7b47b-dddc-445d-918f-02b1b6a37075
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: RevokeActiveObject, RevokeActiveObject function [Automation], _oa96_RevokeActiveObject, automat.revokeactiveobject, oleauto/RevokeActiveObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
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
tech.root: 
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	RevokeActiveObject
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RevokeActiveObject function


## -description


Ends an object's status as active.


## -parameters




### -param dwRegister [in]

A handle previously returned by <a href="https://msdn.microsoft.com/ba15bb69-7b65-47ea-b938-f235e3d9f9ee">RegisterActiveObject</a>.




### -param pvReserved

Reserved for future use. Must be null.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




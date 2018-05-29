---
UID: NF:uiautomationcoreapi.SynchronizedInputPattern_Cancel
title: SynchronizedInputPattern_Cancel function
author: windows-sdk-content
description: Causes the UI Automation provider to stop listening for mouse or keyboard input.
old-location: winauto\uiauto_SynchronizedInputPattern_Cancel.htm
old-project: WinAuto
ms.assetid: e41153c1-5eea-4850-8845-9c3dc07816a3
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: SynchronizedInputPattern_Cancel, SynchronizedInputPattern_Cancel function [Windows Accessibility], uiauto.uiauto_SynchronizedInputPattern_Cancel, uiauto_SynchronizedInputPattern_Cancel, uiautomationcoreapi/SynchronizedInputPattern_Cancel, winauto.uiauto_SynchronizedInputPattern_Cancel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Uiautomationcore.dll
api_name:
-	SynchronizedInputPattern_Cancel
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# SynchronizedInputPattern_Cancel function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Causes the UI Automation provider to stop listening for mouse or keyboard input.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The <i>control pattern</i> object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




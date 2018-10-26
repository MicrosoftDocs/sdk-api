---
UID: NF:uiautomationcoreapi.SynchronizedInputPattern_StartListening
title: SynchronizedInputPattern_StartListening function
author: windows-sdk-content
description: Causes the UI Automation provider to start listening for mouse or keyboard input.
old-location: winauto\uiauto_SynchronizedInputPattern_StartListening.htm
tech.root: WinAuto
ms.assetid: 6c8c88fc-25b2-4ca3-86d7-f1d666fc45e1
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: SynchronizedInputPattern_StartListening, SynchronizedInputPattern_StartListening function [Windows Accessibility], uiauto.uiauto_SynchronizedInputPattern_StartListening, uiauto_SynchronizedInputPattern_StartListening, uiautomationcoreapi/SynchronizedInputPattern_StartListening, winauto.uiauto_SynchronizedInputPattern_StartListening
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - SynchronizedInputPattern_StartListening
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SynchronizedInputPattern_StartListening function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Causes the UI Automation provider to start listening for mouse or keyboard input.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The <i>control pattern</i> object.


### -param inputType [in]

Type: <b><a href="https://msdn.microsoft.com/28c66392-89f0-40eb-be19-ac84c64dacb7">SynchronizedInputType</a></b>

A combination of values from the <a href="https://msdn.microsoft.com/28c66392-89f0-40eb-be19-ac84c64dacb7">SynchronizedInputType</a> enumerated type specifying the type of input for which to listen.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




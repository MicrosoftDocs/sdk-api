---
UID: NF:uiautomationclient.IUIAutomation.SafeArrayToRectNativeArray
title: IUIAutomation::SafeArrayToRectNativeArray (uiautomationclient.h)
author: windows-sdk-content
description: Converts a SAFEARRAY containing rectangle coordinates to an array of type RECT.
old-location: winauto\uiauto_IUIAutomation_SafeArrayToRectNativeArray.htm
tech.root: WinAuto
ms.assetid: 1fa9fad1-55b9-4cb5-a5c2-687074fa5d56
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],SafeArrayToRectNativeArray method, IUIAutomation.SafeArrayToRectNativeArray, IUIAutomation::SafeArrayToRectNativeArray, SafeArrayToRectNativeArray, SafeArrayToRectNativeArray method [Windows Accessibility], SafeArrayToRectNativeArray method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_SafeArrayToRectNativeArray, uiauto_IUIAutomation_SafeArrayToRectNativeArray, uiautomationclient/IUIAutomation::SafeArrayToRectNativeArray, winauto.uiauto_IUIAutomation_SafeArrayToRectNativeArray
ms.topic: method
f1_keywords: ["uiautomationclient/IUIAutomation.SafeArrayToRectNativeArray"]
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.SafeArrayToRectNativeArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::SafeArrayToRectNativeArray


## -description


Converts a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> containing rectangle coordinates to an array of type <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>. 


## -parameters




### -param rects [in]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to an array containing rectangle coordinates.


### -param rectArray [out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>**</b>

Receives a pointer to an array of structures containing rectangle coordinates.


### -param rectArrayCount [out, retval]

Type: <b>int*</b>

Receives the number of elements in <i>rectArray</i>.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




---
UID: NF:uiautomationcore.IAccessibleEx.GetRuntimeId
title: IAccessibleEx::GetRuntimeId (uiautomationcore.h)
author: windows-sdk-content
description: Retrieves the runtime identifier of this element.
old-location: winauto\uiauto_IAccessibleEx_GetRuntimeId.htm
tech.root: WinAuto
ms.assetid: 00aeac66-398a-4c80-85e2-32bff0ae100f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRuntimeId, GetRuntimeId method [Windows Accessibility], GetRuntimeId method [Windows Accessibility],IAccessibleEx interface, IAccessibleEx interface [Windows Accessibility],GetRuntimeId method, IAccessibleEx.GetRuntimeId, IAccessibleEx::GetRuntimeId, uiauto.uiauto_IAccessibleEx_GetRuntimeId, uiauto_IAccessibleEx_GetRuntimeId, uiautomationcore/IAccessibleEx::GetRuntimeId, winauto.uiauto_IAccessibleEx_GetRuntimeId
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - UIAutomationCore.h
api_name:
 - IAccessibleEx.GetRuntimeId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibleEx::GetRuntimeId


## -description


Retrieves the runtime identifier of this element.


## -parameters




### -param pRetVal [out]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to the runtime identifier.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The runtime identifier is a provider-defined array of integers, the first item of which must be <b>UiaAppendRuntimeId</b>. The runtime identifier must be unique within the parent window.

The MSAA-to-UIA Proxy uses the runtime identifier (together with the window handle) to determine if two interface instances refer to the same underlying element. If <b>IAccessibleEx::GetRuntimeId</b> is not implemented, the proxy performs field-by-field comparisons on the two <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> objects to determine if they are equivalent, which is less efficient.
            




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a>



<b>Reference</b>
 

 


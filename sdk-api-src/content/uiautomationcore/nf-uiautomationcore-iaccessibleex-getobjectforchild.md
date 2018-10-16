---
UID: NF:uiautomationcore.IAccessibleEx.GetObjectForChild
title: IAccessibleEx::GetObjectForChild
author: windows-sdk-content
description: Retrieves an IAccessibleEx interface representing the specified child of this element.
old-location: winauto\uiauto_IAccessibleEx_GetObjectForChild.htm
tech.root: WinAuto
ms.assetid: fbb279cc-2224-437e-875b-d08df175edf1
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetObjectForChild, GetObjectForChild method [Windows Accessibility], GetObjectForChild method [Windows Accessibility],IAccessibleEx interface, IAccessibleEx interface [Windows Accessibility],GetObjectForChild method, IAccessibleEx.GetObjectForChild, IAccessibleEx::GetObjectForChild, uiauto.uiauto_IAccessibleEx_GetObjectForChild, uiauto_IAccessibleEx_GetObjectForChild, uiautomationcore/IAccessibleEx::GetObjectForChild, winauto.uiauto_IAccessibleEx_GetObjectForChild
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAccessibleEx.GetObjectForChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibleEx::GetObjectForChild


## -description


Retrieves an <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> interface representing the specified child of this element.


## -parameters




### -param idChild [in]

Type: <b>long</b>

The identifier of the child element.


### -param pRetVal [out]

Type: <b><a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a>**</b>

Receives a pointer to the <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<i>pRetVal</i> returns <b>NULL</b> if this implementation does not use child IDs, or cannot provide an <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> interface for the specified child, or itself represents a child element.

<i>idChild</i> must represent an actual MSAA child element, not an object that has its own <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a>
 

 


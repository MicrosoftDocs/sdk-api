---
UID: NF:uiautomationcore.IValueProvider.SetValue
title: IValueProvider::SetValue
author: windows-sdk-content
description: Sets the value of control.
old-location: winauto\uiauto_IValueProvider_SetValue.htm
tech.root: WinAuto
ms.assetid: af555ac6-5abd-4019-804b-68f9ed3be801
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IValueProvider interface [Windows Accessibility],SetValue method, IValueProvider.SetValue, IValueProvider::SetValue, SetValue, SetValue method [Windows Accessibility], SetValue method [Windows Accessibility],IValueProvider interface, uiauto.uiauto_IValueProvider_SetValue, uiauto_IValueProvider_SetValue, uiautomationcore/IValueProvider::SetValue, winauto.uiauto_IValueProvider_SetValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - IValueProvider.SetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IValueProvider::SetValue


## -description


Sets the value of control.


## -parameters




### -param val [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The value to set. The provider is responsible for converting the value to the appropriate data type.



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Single-line edit controls support programmatic access to their contents by implementing <a href="https://msdn.microsoft.com/e6adbc23-dbfe-4dd2-82d9-66ce16de3338">IValueProvider</a>. 
        However, multi-line edit controls do not implement <b>IValueProvider</b>; 
        instead they provide access to their content by implementing <a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>.
        

Controls such as ListItem and TreeItem must implement <a href="https://msdn.microsoft.com/e6adbc23-dbfe-4dd2-82d9-66ce16de3338">IValueProvider</a> 
        if the value of any of the items is editable, regardless of the current edit 
        mode of the control. The parent control must also implement <b>IValueProvider</b> 
        if the child items are editable. 
        




## -see-also




<a href="https://msdn.microsoft.com/e6adbc23-dbfe-4dd2-82d9-66ce16de3338">IValueProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 


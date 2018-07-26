---
UID: NF:uiautomationcore.IRangeValueProvider.SetValue
title: IRangeValueProvider::SetValue
author: windows-sdk-content
description: Sets the value of the control.
old-location: winauto\uiauto_IRangeValueProvider_SetValue.htm
old-project: WinAuto
ms.assetid: 3ce214a0-e7ff-440a-a308-fea5608e13f0
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IRangeValueProvider interface [Windows Accessibility],SetValue method, IRangeValueProvider.SetValue, IRangeValueProvider::SetValue, SetValue, SetValue method [Windows Accessibility], SetValue method [Windows Accessibility],IRangeValueProvider interface, uiauto.uiauto_IRangeValueProvider_SetValue, uiauto_IRangeValueProvider_SetValue, uiautomationcore/IRangeValueProvider::SetValue, winauto.uiauto_IRangeValueProvider_SetValue
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IRangeValueProvider.SetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRangeValueProvider::SetValue


## -description


Sets the value of the control.


## -parameters




### -param val [in]

Type: <b>double</b>

The value to set.



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The actual value set depends on the control implementation. The control may round the requested value up or down.
		




## -see-also




<a href="https://msdn.microsoft.com/1e9e39f9-e728-4ed6-bc62-80d3bbe6302d">IRangeValueProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 


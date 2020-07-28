---
UID: NF:uiautomationcore.IRangeValueProvider.get_SmallChange
title: IRangeValueProvider::get_SmallChange (uiautomationcore.h)
description: Specifies the value that is added to or subtracted from the IRangeValueProvider::Value property when a small change is made, such as when an arrow key is pressed.
helpviewer_keywords: ["IRangeValueProvider interface [Windows Accessibility]","SmallChange property","IRangeValueProvider.SmallChange","IRangeValueProvider.get_SmallChange","IRangeValueProvider::SmallChange","IRangeValueProvider::get_SmallChange","SmallChange property [Windows Accessibility]","SmallChange property [Windows Accessibility]","IRangeValueProvider interface","get_SmallChange","uiauto.uiauto_IRangeValueProvider_SmallChange","uiauto_IRangeValueProvider_SmallChange","uiautomationcore/IRangeValueProvider::SmallChange","uiautomationcore/IRangeValueProvider::get_SmallChange","winauto.uiauto_IRangeValueProvider_SmallChange"]
old-location: winauto\uiauto_IRangeValueProvider_SmallChange.htm
tech.root: WinAuto
ms.assetid: 8230747d-d8c3-4708-a77a-7c76a62f39dd
ms.date: 12/05/2018
ms.keywords: IRangeValueProvider interface [Windows Accessibility],SmallChange property, IRangeValueProvider.SmallChange, IRangeValueProvider.get_SmallChange, IRangeValueProvider::SmallChange, IRangeValueProvider::get_SmallChange, SmallChange property [Windows Accessibility], SmallChange property [Windows Accessibility],IRangeValueProvider interface, get_SmallChange, uiauto.uiauto_IRangeValueProvider_SmallChange, uiauto_IRangeValueProvider_SmallChange, uiautomationcore/IRangeValueProvider::SmallChange, uiautomationcore/IRangeValueProvider::get_SmallChange, winauto.uiauto_IRangeValueProvider_SmallChange
f1_keywords:
- uiautomationcore/IRangeValueProvider.SmallChange
dev_langs:
- c++
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
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uiautomationcore.dll
api_name:
- IRangeValueProvider.SmallChange
- IRangeValueProvider.get_SmallChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRangeValueProvider::get_SmallChange


## -description


Specifies the value that is added to or subtracted from the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-get_value">IRangeValueProvider::Value</a> property 
        when a small change is made, such as when an arrow key is pressed.
        

This property is read-only.


## -parameters


## -remarks



The SmallChange property can support Not a Number (NaN) value. When returning a NaN value, the provider should return a quiet (non-signaling) NaN to avoid raising an exception if floating-point exceptions are turned on. The following example shows how to create a quiet NaN:

            


```
ULONGLONG ulNaN = 0xFFFFFFFFFFFFFFFF;
    *pRetVal = *reinterpret_cast<double*>(&ulNaN);
```


Alternatively, you can use the following function from the standard C++ libraries:


```
numeric_limits<double>::quiet_NaN( )
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irangevalueprovider">IRangeValueProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 


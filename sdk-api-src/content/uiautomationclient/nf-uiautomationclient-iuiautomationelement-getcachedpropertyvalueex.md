---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedPropertyValueEx
title: IUIAutomationElement::GetCachedPropertyValueEx
author: windows-sdk-content
description: Retrieves a property value from the cache for this UI Automation element, optionally ignoring any default value.
old-location: winauto\uiauto_IUIAutomationElement_GetCachedPropertyValueEx.htm
tech.root: WinAuto
ms.assetid: 3f496ee4-8508-4331-9c1c-7805e17874f9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetCachedPropertyValueEx, GetCachedPropertyValueEx method [Windows Accessibility], GetCachedPropertyValueEx method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedPropertyValueEx method, IUIAutomationElement.GetCachedPropertyValueEx, IUIAutomationElement::GetCachedPropertyValueEx, uiauto.uiauto_IUIAutomationElement_GetCachedPropertyValueEx, uiauto_IUIAutomationElement_GetCachedPropertyValueEx, uiautomationclient/IUIAutomationElement::GetCachedPropertyValueEx, winauto.uiauto_IUIAutomationElement_GetCachedPropertyValueEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IUIAutomationElement.GetCachedPropertyValueEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationElement::GetCachedPropertyValueEx


## -description


Retrieves a property value from the cache for this UI Automation element, optionally ignoring any default value.


## -parameters




### -param propertyId [in]

Type: <b>PROPERTYID</b>

The identifier of the property. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>. 


### -param ignoreDefaultValue [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A value that specifies whether a default value should be ignored if the specified property is not supported: <b>TRUE</b> if the default value is not to be returned, or <b>FALSE</b> if it is to be returned.


### -param retVal [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-tagvariant">VARIANT</a>*</b>

Receives the value of the property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method retrieves the specified property from the cache for the UI Automation element. To retrieve the current property, call <a href="https://msdn.microsoft.com/3adbd380-4500-4701-bfc3-dc03d51e5155">IUIAutomationElement::GetCurrentPropertyValueEx</a>.

Passing <b>FALSE</b> in the <i>ignoreDefaultValue</i> parameter is equivalent to calling <a href="https://msdn.microsoft.com/3cd093fe-04ee-4b09-b5e7-28dad984951e">IUIAutomationElement::GetCachedPropertyValue</a>.

If the Microsoft UI Automation provider for the element itself supports the property, the value of the property is returned. Otherwise, if <i>ignoreDefaultValue</i> is <b>FALSE</b>, a default value specified by UI Automation is returned. 

This method returns a failure code  if the requested property was not previously cached.

UI Automation properties of the <b>double</b> type support Not a Number (NaN) values. When retrieving a property of the <b>double</b> type, a client can use the <a href="https://go.microsoft.com/fwlink/p/?linkid=198403">_isnan</a> function to determine whether the property is a NaN value.
        




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3cd093fe-04ee-4b09-b5e7-28dad984951e">GetCachedPropertyValue</a>



<a href="https://msdn.microsoft.com/3adbd380-4500-4701-bfc3-dc03d51e5155">GetCurrentPropertyValueEx</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/35f017cb-f50a-4680-9f01-5079aa59da73">UI Automation Properties Overview</a>
 

 


---
UID: NF:uiautomationclient.IUIAutomationElement.GetCurrentPropertyValueEx
title: IUIAutomationElement::GetCurrentPropertyValueEx method
author: windows-driver-content
description: Retrieves a property value for this UI Automation element, optionally ignoring any default value.
old-location: winauto\uiauto_IUIAutomationElement_GetCurrentPropertyValueEx.htm
old-project: WinAuto
ms.assetid: 3adbd380-4500-4701-bfc3-dc03d51e5155
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetCurrentPropertyValueEx method [Windows Accessibility], GetCurrentPropertyValueEx method [Windows Accessibility], IUIAutomationElement interface, GetCurrentPropertyValueEx,IUIAutomationElement.GetCurrentPropertyValueEx, IUIAutomationElement, IUIAutomationElement interface [Windows Accessibility], GetCurrentPropertyValueEx method, IUIAutomationElement::GetCurrentPropertyValueEx, uiauto.uiauto_IUIAutomationElement_GetCurrentPropertyValueEx, uiauto_IUIAutomationElement_GetCurrentPropertyValueEx, uiautomationclient/IUIAutomationElement::GetCurrentPropertyValueEx, winauto.uiauto_IUIAutomationElement_GetCurrentPropertyValueEx
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomationElement.GetCurrentPropertyValueEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationElement::GetCurrentPropertyValueEx method


## -description


Retrieves a property value for this UI Automation element, optionally ignoring any default value.


## -parameters




### -param propertyId [in]

Type: <b>PROPERTYID</b>

The identifier of the property. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param ignoreDefaultValue [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A value that specifies whether a default value should be ignored if the specified property is not supported: <b>TRUE</b> if the default value is not to be returned, or <b>FALSE</b> if it is to be returned.


### -param retVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>*</b>

Receives the property value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Passing <b>FALSE</b> in the <i>ignoreDefaultValue</i> parameter is equivalent to calling <a href="https://msdn.microsoft.com/819e548e-7ff4-4f9f-969b-bfd1625f6151">IUIAutomationElement::GetCurrentPropertyValue</a>.

If the Microsoft UI Automation provider for the element itself supports the property, the value of the property is returned. Otherwise, if <i>ignoreDefaultValue</i> is <b>FALSE</b>, a default value specified by UI Automation is returned. 

 This method returns a failure code if the requested property was not previously cached.

UI Automation properties of the <b>double</b> type support Not a Number (NaN) values. When retrieving a property of the <b>double</b> type, a client can use the <a href="http://go.microsoft.com/fwlink/p/?linkid=198403">_isnan</a> function to determine whether the property is a NaN value.
        




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3f496ee4-8508-4331-9c1c-7805e17874f9">GetCachedPropertyValueEx</a>



<a href="https://msdn.microsoft.com/819e548e-7ff4-4f9f-969b-bfd1625f6151">GetCurrentPropertyValue</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/35f017cb-f50a-4680-9f01-5079aa59da73">UI Automation Properties Overview</a>
 

 


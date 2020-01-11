---
UID: NF:uiautomationclient.IUIAutomationElement.GetCurrentPropertyValueEx
title: IUIAutomationElement::GetCurrentPropertyValueEx (uiautomationclient.h)
description: Retrieves a property value for this UI Automation element, optionally ignoring any default value.
old-location: winauto\uiauto_IUIAutomationElement_GetCurrentPropertyValueEx.htm
tech.root: WinAuto
ms.assetid: 3adbd380-4500-4701-bfc3-dc03d51e5155
ms.date: 12/05/2018
ms.keywords: GetCurrentPropertyValueEx, GetCurrentPropertyValueEx method [Windows Accessibility], GetCurrentPropertyValueEx method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCurrentPropertyValueEx method, IUIAutomationElement.GetCurrentPropertyValueEx, IUIAutomationElement::GetCurrentPropertyValueEx, uiauto.uiauto_IUIAutomationElement_GetCurrentPropertyValueEx, uiauto_IUIAutomationElement_GetCurrentPropertyValueEx, uiautomationclient/IUIAutomationElement::GetCurrentPropertyValueEx, winauto.uiauto_IUIAutomationElement_GetCurrentPropertyValueEx
f1_keywords:
- uiautomationclient/IUIAutomationElement.GetCurrentPropertyValueEx
dev_langs:
- c++
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
- IUIAutomationElement.GetCurrentPropertyValueEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationElement::GetCurrentPropertyValueEx


## -description


Retrieves a property value for this UI Automation element, optionally ignoring any default value.


## -parameters




### -param propertyId [in]

Type: <b>PROPERTYID</b>

The identifier of the property. For a list of property IDs, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.


### -param ignoreDefaultValue [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A value that specifies whether a default value should be ignored if the specified property is not supported: <b>TRUE</b> if the default value is not to be returned, or <b>FALSE</b> if it is to be returned.


### -param retVal [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>*</b>

Receives the property value.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Passing <b>FALSE</b> in the <i>ignoreDefaultValue</i> parameter is equivalent to calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue">IUIAutomationElement::GetCurrentPropertyValue</a>.

If the Microsoft UI Automation provider for the element itself supports the property, the value of the property is returned. Otherwise, if <i>ignoreDefaultValue</i> is <b>FALSE</b>, a default value specified by UI Automation is returned. 

 This method returns a failure code if the requested property was not previously cached.

UI Automation properties of the <b>double</b> type support Not a Number (NaN) values. When retrieving a property of the <b>double</b> type, a client can use the <a href="https://go.microsoft.com/fwlink/p/?linkid=198403">_isnan</a> function to determine whether the property is a NaN value.
        




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex">GetCachedPropertyValueEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue">GetCurrentPropertyValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-propertiesoverview">UI Automation Properties Overview</a>
 

 


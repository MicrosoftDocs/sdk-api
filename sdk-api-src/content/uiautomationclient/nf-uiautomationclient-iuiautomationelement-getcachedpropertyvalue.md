---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedPropertyValue
title: IUIAutomationElement::GetCachedPropertyValue (uiautomationclient.h)
description: Retrieves a property value from the cache for this UI Automation element.
helpviewer_keywords: ["GetCachedPropertyValue","GetCachedPropertyValue method [Windows Accessibility]","GetCachedPropertyValue method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","GetCachedPropertyValue method","IUIAutomationElement.GetCachedPropertyValue","IUIAutomationElement::GetCachedPropertyValue","uiauto.uiauto_IUIAutomationElement_GetCachedPropertyValue","uiauto_IUIAutomationElement_GetCachedPropertyValue","uiautomationclient/IUIAutomationElement::GetCachedPropertyValue","winauto.uiauto_IUIAutomationElement_GetCachedPropertyValue"]
old-location: winauto\uiauto_IUIAutomationElement_GetCachedPropertyValue.htm
tech.root: WinAuto
ms.assetid: 3cd093fe-04ee-4b09-b5e7-28dad984951e
ms.date: 12/05/2018
ms.keywords: GetCachedPropertyValue, GetCachedPropertyValue method [Windows Accessibility], GetCachedPropertyValue method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedPropertyValue method, IUIAutomationElement.GetCachedPropertyValue, IUIAutomationElement::GetCachedPropertyValue, uiauto.uiauto_IUIAutomationElement_GetCachedPropertyValue, uiauto_IUIAutomationElement_GetCachedPropertyValue, uiautomationclient/IUIAutomationElement::GetCachedPropertyValue, winauto.uiauto_IUIAutomationElement_GetCachedPropertyValue
f1_keywords:
- uiautomationclient/IUIAutomationElement.GetCachedPropertyValue
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
- IUIAutomationElement.GetCachedPropertyValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationElement::GetCachedPropertyValue


## -description


Retrieves a property value from the cache for this UI Automation element.


## -parameters




### -param propertyId [in]

Type: <b>PROPERTYID</b>

The identifier of the property.  For a list of property IDs, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>. 


### -param retVal [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>*</b>

Receives the value of the cached property.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Microsoft UI Automation properties of the <b>double</b> type support Not a Number (NaN) values. When retrieving a property of the <b>double</b> type, a client can use the <a href="https://msdn.microsoft.com/library/aa298428(VS.60).aspx">_isnan</a> function to determine whether the property is a NaN value.
        




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex">GetCachedPropertyValueEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue">GetCurrentPropertyValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-propertiesoverview">UI Automation Properties Overview</a>
 

 


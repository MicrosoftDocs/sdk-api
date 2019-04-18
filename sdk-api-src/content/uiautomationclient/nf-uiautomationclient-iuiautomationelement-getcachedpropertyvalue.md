---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedPropertyValue
title: IUIAutomationElement::GetCachedPropertyValue (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves a property value from the cache for this UI Automation element.
old-location: winauto\uiauto_IUIAutomationElement_GetCachedPropertyValue.htm
tech.root: WinAuto
ms.assetid: 3cd093fe-04ee-4b09-b5e7-28dad984951e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCachedPropertyValue, GetCachedPropertyValue method [Windows Accessibility], GetCachedPropertyValue method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedPropertyValue method, IUIAutomationElement.GetCachedPropertyValue, IUIAutomationElement::GetCachedPropertyValue, uiauto.uiauto_IUIAutomationElement_GetCachedPropertyValue, uiauto_IUIAutomationElement_GetCachedPropertyValue, uiautomationclient/IUIAutomationElement::GetCachedPropertyValue, winauto.uiauto_IUIAutomationElement_GetCachedPropertyValue
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
 - IUIAutomationElement.GetCachedPropertyValue
product: Windows
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

The identifier of the property.  For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>. 


### -param retVal [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-tagvariant">VARIANT</a>*</b>

Receives the value of the cached property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Microsoft UI Automation properties of the <b>double</b> type support Not a Number (NaN) values. When retrieving a property of the <b>double</b> type, a client can use the <a href="https://go.microsoft.com/fwlink/p/?linkid=198403">_isnan</a> function to determine whether the property is a NaN value.
        




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3f496ee4-8508-4331-9c1c-7805e17874f9">GetCachedPropertyValueEx</a>



<a href="https://msdn.microsoft.com/819e548e-7ff4-4f9f-969b-bfd1625f6151">GetCurrentPropertyValue</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/35f017cb-f50a-4680-9f01-5079aa59da73">UI Automation Properties Overview</a>
 

 


---
UID: NF:uiautomationclient.IUIAutomation.CreatePropertyCondition
title: IUIAutomation::CreatePropertyCondition (uiautomationclient.h)
author: windows-sdk-content
description: Creates a condition that selects elements that have a property with the specified value.
old-location: winauto\uiauto_IUIAutomation_CreatePropertyCondition.htm
tech.root: WinAuto
ms.assetid: 8b777a53-90a8-4e51-b707-d0ea8f5790a8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreatePropertyCondition, CreatePropertyCondition method [Windows Accessibility], CreatePropertyCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreatePropertyCondition method, IUIAutomation.CreatePropertyCondition, IUIAutomation::CreatePropertyCondition, uiauto.uiauto_IUIAutomation_CreatePropertyCondition, uiauto_IUIAutomation_CreatePropertyCondition, uiautomationclient/IUIAutomation::CreatePropertyCondition, winauto.uiauto_IUIAutomation_CreatePropertyCondition
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
 - IUIAutomation.CreatePropertyCondition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::CreatePropertyCondition


## -description


Creates a condition that selects elements that have a property with the specified value.


## -parameters




### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier.  For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param value [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-tagvariant">VARIANT</a></b>

The property value.


### -param newCondition [out, retval]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>**</b>

Receives a pointer to the new condition.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/dc7ad9e8-b315-40b1-af02-997a38c4ee66">CreatePropertyConditionEx</a>



<a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a>



<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>



<a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a>



<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>



<b>Reference</b>
 

 


---
UID: NF:uiautomationcoreapi.UiaLookupId
title: UiaLookupId function
author: windows-sdk-content
description: Gets the integer identifier that can be used in methods that require a PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID, or EVENTID.
old-location: winauto\uiauto_UiaLookupIdAutoMeth.htm
old-project: WinAuto
ms.assetid: 9906acea-5246-4f01-8d76-03b89ff2f789
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: UiaLookupId, UiaLookupId function [Windows Accessibility], uiauto.uiauto_UiaLookupIdAutoMeth, uiauto_UiaLookupIdAutoMeth, uiautomationcoreapi/UiaLookupId, winauto.uiauto_UiaLookupIdAutoMeth
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Uiautomationcore.dll
-	Ext-MS-Win-uiacore-l1-1-0.dll
-	Ext-MS-Win-UIaCore-l1-1-1.dll
-	Ext-MS-Win-UIaCore-l1-1-2.dll
-	Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
-	UiaLookupId
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaLookupId function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets the integer identifier that can be used in methods that require a PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID, or EVENTID.


## -parameters




### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/798afc92-73bc-4a76-a8bb-afa804038205">AutomationIdentifierType</a></b>

A value from the <a href="https://msdn.microsoft.com/798afc92-73bc-4a76-a8bb-afa804038205">AutomationIdentifierType</a> enumerated type that specifies the type of identifier to look up.


### -param pGuid [in]

Type: <b>GUID*</b>

The address of the unique identifier of the property, pattern, control type, text attribute, or event.


## -returns



Type: <b>int</b>

Returns an integer identifier.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b8e9e33c-9781-4f50-bbb7-a9950409f2e6">GUIDs</a>



<a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>
 

 


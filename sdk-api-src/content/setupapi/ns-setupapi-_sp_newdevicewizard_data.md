---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SP_NEWDEVICEWIZARD_DATA structure


## -description


An installer uses an SP_ADDPROPERTYPAGE_DATA structure to supply custom property pages for a device when it handles a DIF_ADDPROPERTYPAGE_ADVANCED request. 


## -struct-fields




### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request.


### -field Flags

Reserved. Must be zero.


### -field DynamicPages

An array of property sheet page handles. An installer can add the handles of custom property pages to this array.


### -field NumDynamicPages

The number of pages that are added to the<b> DynamicPages</b> array. 

Because the array index is zero-based, this value is also the index to the next free entry in the array. For example, if there are three pages in the array, <b>DynamicPages[</b>3<b>]</b> is the next entry for an installer to use.


### -field hwndWizardDlg

The handle to the Device Manager top-level window.


## -remarks



See the Microsoft Windows SDK for documentation on the PROPSHEETPAGE structure and for more information about property pages.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543656">DIF_ADDPROPERTYPAGE_ADVANCED</a>
 

 


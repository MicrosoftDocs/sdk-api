---
UID: NS:setupapi._SP_NEWDEVICEWIZARD_DATA
title: "_SP_NEWDEVICEWIZARD_DATA"
author: windows-sdk-content
description: An installer uses an SP_ADDPROPERTYPAGE_DATA structure to supply custom property pages for a device when it handles a DIF_ADDPROPERTYPAGE_ADVANCED request.
old-location: devinst\sp_addpropertypage_data.htm
old-project: devinst
ms.assetid: 065c83b1-4b5d-4988-871a-48b0f8b14be7
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: "*PSP_NEWDEVICEWIZARD_DATA, PSP_ADDPROPERTYPAGE_DATA, PSP_ADDPROPERTYPAGE_DATA structure pointer [Device and Driver Installation], SP_ADDPROPERTYPAGE_DATA, SP_ADDPROPERTYPAGE_DATA structure [Device and Driver Installation], SP_NEWDEVICEWIZARD_DATA, _SP_NEWDEVICEWIZARD_DATA, devinst.sp_addpropertypage_data, di-struct_d555aae2-5898-4b20-b20c-163ff3ee2cdd.xml, setupapi/PSP_ADDPROPERTYPAGE_DATA, setupapi/SP_ADDPROPERTYPAGE_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
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
tech.root: 
req.typenames: SP_NEWDEVICEWIZARD_DATA, *PSP_NEWDEVICEWIZARD_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - SP_ADDPROPERTYPAGE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 


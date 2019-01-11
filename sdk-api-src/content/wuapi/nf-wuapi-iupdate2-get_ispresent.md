---
UID: NF:wuapi.IUpdate2.get_IsPresent
title: IUpdate2::get_IsPresent
author: windows-sdk-content
description: Gets a Boolean value that indicates whether an update is present on a computer.
old-location: wua\iupdate2_ispresent.htm
tech.root: Wua_Sdk
ms.assetid: de378d24-aba9-44c2-9c49-fbd1b2fc2446
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUpdate2 interface [Windows Update Agent],IsPresent property, IUpdate2.IsPresent, IUpdate2.get_IsPresent, IUpdate2::IsPresent, IUpdate2::get_IsPresent, IsPresent property [Windows Update Agent], IsPresent property [Windows Update Agent],IUpdate2 interface, get_IsPresent, wua.iupdate2_ispresent, wuapi/IUpdate2::IsPresent, wuapi/IUpdate2::get_IsPresent
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate2.IsPresent
 - IUpdate2.get_IsPresent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdate2::get_IsPresent


## -description


Gets a Boolean value that indicates whether an update is present on a computer.

This property is read-only.


## -parameters


## -remarks



An update is considered present if it is installed for one or more products. For example, if an update applies to both Microsoft Office Word and to Microsoft Office Excel, the <b>IsPresent</b> property returns <b>VARIANT_TRUE</b> if the update is installed for one or both of the products.

If an update applies to only one product, the <b>IsPresent</b> and <a href="https://msdn.microsoft.com/2adebe8e-554e-4337-9bbf-1d8967fefef1">IsInstalled</a> properties are equivalent. An update is considered installed if the update is installed for all the products to which it applies.

If <b>IsPresent</b> returns <b>VARIANT_TRUE</b> and <a href="https://msdn.microsoft.com/2adebe8e-554e-4337-9bbf-1d8967fefef1">IsInstalled</a> returns <b>VARIANT_FALSE</b>, the update can be uninstalled for the product that installed it.




## -see-also




<a href="https://msdn.microsoft.com/75041e85-0f3c-4996-9af2-d2969549393e">IUpdate2</a>
 

 


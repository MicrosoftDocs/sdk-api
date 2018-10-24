---
UID: NF:propsys.IPropertyDescriptionSearchInfo.GetSearchInfoFlags
title: IPropertyDescriptionSearchInfo::GetSearchInfoFlags
author: windows-sdk-content
description: Gets the PROPDESC_SEARCHINFO_FLAGS associated with the property.
old-location: properties\IPropertyDescriptionSearchInfo_GetSearchInfoFlags.htm
tech.root: properties
ms.assetid: 37abf6c3-700b-4dbe-9701-c40a3d254a8c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetSearchInfoFlags, GetSearchInfoFlags method [Windows Properties], GetSearchInfoFlags method [Windows Properties],IPropertyDescriptionSearchInfo interface, IPropertyDescriptionSearchInfo interface [Windows Properties],GetSearchInfoFlags method, IPropertyDescriptionSearchInfo.GetSearchInfoFlags, IPropertyDescriptionSearchInfo::GetSearchInfoFlags, _shell_IPropertyDescriptionSearchInfo_GetSearchInfoFlags, properties.IPropertyDescriptionSearchInfo_GetSearchInfoFlags, propsys/IPropertyDescriptionSearchInfo::GetSearchInfoFlags, shell.IPropertyDescriptionSearchInfo_GetSearchInfoFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - Propsys.h
api_name:
 - IPropertyDescriptionSearchInfo.GetSearchInfoFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescriptionSearchInfo::GetSearchInfoFlags


## -description


Gets the <a href="https://msdn.microsoft.com/en-us/library/Bb762588(v=VS.85).aspx">PROPDESC_SEARCHINFO_FLAGS</a> associated with the property.


## -parameters




### -param ppdsiFlags [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762588(v=VS.85).aspx">PROPDESC_SEARCHINFO_FLAGS</a>*</b>

When this method returns successfully, contains a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb762588(v=VS.85).aspx">PROPDESC_SEARCHINFO_FLAGS</a> associated with the property.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761505(v=VS.85).aspx">IPropertyDescriptionSearchInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762588(v=VS.85).aspx">PROPDESC_SEARCHINFO_FLAGS</a>
 

 


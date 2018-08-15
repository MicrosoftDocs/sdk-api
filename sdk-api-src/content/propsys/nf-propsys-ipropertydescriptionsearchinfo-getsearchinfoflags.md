---
UID: NF:propsys.IPropertyDescriptionSearchInfo.GetSearchInfoFlags
title: IPropertyDescriptionSearchInfo::GetSearchInfoFlags
author: windows-sdk-content
description: Gets the PROPDESC_SEARCHINFO_FLAGS associated with the property.
old-location: properties\IPropertyDescriptionSearchInfo_GetSearchInfoFlags.htm
old-project: properties
ms.assetid: 37abf6c3-700b-4dbe-9701-c40a3d254a8c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetSearchInfoFlags, GetSearchInfoFlags method [Windows Properties], GetSearchInfoFlags method [Windows Properties],IPropertyDescriptionSearchInfo interface, IPropertyDescriptionSearchInfo interface [Windows Properties],GetSearchInfoFlags method, IPropertyDescriptionSearchInfo.GetSearchInfoFlags, IPropertyDescriptionSearchInfo::GetSearchInfoFlags, _shell_IPropertyDescriptionSearchInfo_GetSearchInfoFlags, properties.IPropertyDescriptionSearchInfo_GetSearchInfoFlags, propsys/IPropertyDescriptionSearchInfo::GetSearchInfoFlags, shell.IPropertyDescriptionSearchInfo_GetSearchInfoFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propsys.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PSC_STATE
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescriptionSearchInfo::GetSearchInfoFlags


## -description


Gets the <a href="shell.PROPDESC_SEARCHINFO_FLAGS">PROPDESC_SEARCHINFO_FLAGS</a> associated with the property.


## -parameters




### -param ppdsiFlags [out]

Type: <b><a href="shell.PROPDESC_SEARCHINFO_FLAGS">PROPDESC_SEARCHINFO_FLAGS</a>*</b>

When this method returns successfully, contains a pointer to the <a href="shell.PROPDESC_SEARCHINFO_FLAGS">PROPDESC_SEARCHINFO_FLAGS</a> associated with the property.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="shell.IPropertyDescriptionSearchInfo">IPropertyDescriptionSearchInfo</a>



<a href="shell.PROPDESC_SEARCHINFO_FLAGS">PROPDESC_SEARCHINFO_FLAGS</a>
 

 


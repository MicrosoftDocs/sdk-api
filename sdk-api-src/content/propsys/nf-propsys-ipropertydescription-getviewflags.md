---
UID: NF:propsys.IPropertyDescription.GetViewFlags
title: IPropertyDescription::GetViewFlags
author: windows-sdk-content
description: Gets the current set of flags governing the property's view.
old-location: properties\IPropertyDescription_GetViewFlags.htm
old-project: properties
ms.assetid: 73b60861-3d73-4bff-ae46-a7683d708c83
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetViewFlags, GetViewFlags method [Windows Properties], GetViewFlags method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetViewFlags method, IPropertyDescription.GetViewFlags, IPropertyDescription::GetViewFlags, properties.IPropertyDescription_GetViewFlags, propsys/IPropertyDescription::GetViewFlags, shell.IPropertyDescription_GetViewFlags, shell_IPropertyDescription_GetViewFlags
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
 - IPropertyDescription.GetViewFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescription::GetViewFlags


## -description


Gets the current set of flags governing the property's view.


## -parameters




### -param ppdvFlags [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762528(v=VS.85).aspx">PROPDESC_VIEW_FLAGS</a>*</b>

When this method returns, contains a pointer to a value that includes one or more of the following flags. See <a href="https://msdn.microsoft.com/en-us/library/Bb762528(v=VS.85).aspx">PROPDESC_VIEW_FLAGS</a> for valid values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 


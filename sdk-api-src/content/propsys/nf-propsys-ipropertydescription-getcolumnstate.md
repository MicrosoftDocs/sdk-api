---
UID: NF:propsys.IPropertyDescription.GetColumnState
title: IPropertyDescription::GetColumnState
author: windows-sdk-content
description: Gets the column state flag, which describes how the property should be treated by interfaces or APIs that use this flag.
old-location: properties\IPropertyDescription_GetColumnState.htm
old-project: properties
ms.assetid: fcfb5905-884a-49ed-aa1d-acd3b95753bf
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetColumnState, GetColumnState method [Windows Properties], GetColumnState method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetColumnState method, IPropertyDescription.GetColumnState, IPropertyDescription::GetColumnState, properties.IPropertyDescription_GetColumnState, propsys/IPropertyDescription::GetColumnState, shell.IPropertyDescription_GetColumnState, shell_IPropertyDescription_GetColumnState
ms.prod: windows
ms.technology: windows-sdk
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
 - IPropertyDescription.GetColumnState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescription::GetColumnState


## -description


Gets the column state flag, which describes how the property should be treated by interfaces or APIs that use this flag.


## -parameters




### -param pcsFlags






#### - pcsflags [out]

Type: <b>SHCOLSTATEF</b>

When this method returns, contains a pointer to the column state flag. See <a href="https://msdn.microsoft.com/0dee8474-0ae2-41fc-ad58-02d900039ff6">SHCOLSTATE</a> for valid values.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



The value retrieved by this method is originally set through the <i>displayType</i> attribute of the <a href="shell.propdesc_schema_displayInfo">displayInfo</a> element in the property's .propdesc file.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 


---
UID: NF:propsys.IPropertySystem.RefreshPropertySchema
title: IPropertySystem::RefreshPropertySchema (propsys.h)
description: Not supported. (IPropertySystem.RefreshPropertySchema)
helpviewer_keywords: ["IPropertySystem interface [Windows Properties]","RefreshPropertySchema method","IPropertySystem.RefreshPropertySchema","IPropertySystem::RefreshPropertySchema","RefreshPropertySchema","RefreshPropertySchema method [Windows Properties]","RefreshPropertySchema method [Windows Properties]","IPropertySystem interface","properties.IPropertySystem_RefreshPropertySchema","propsys/IPropertySystem::RefreshPropertySchema","shell.IPropertySystem_RefreshPropertySchema","shell_IPropertySystem_RefreshPropertySchema"]
old-location: properties\IPropertySystem_RefreshPropertySchema.htm
tech.root: properties
ms.assetid: 9aa0c678-5139-42a4-ac71-deb39dae4129
ms.date: 12/05/2018
ms.keywords: IPropertySystem interface [Windows Properties],RefreshPropertySchema method, IPropertySystem.RefreshPropertySchema, IPropertySystem::RefreshPropertySchema, RefreshPropertySchema, RefreshPropertySchema method [Windows Properties], RefreshPropertySchema method [Windows Properties],IPropertySystem interface, properties.IPropertySystem_RefreshPropertySchema, propsys/IPropertySystem::RefreshPropertySchema, shell.IPropertySystem_RefreshPropertySchema, shell_IPropertySystem_RefreshPropertySchema
req.header: propsys.h
req.include-header: Propsys.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: Propsys.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IPropertySystem::RefreshPropertySchema
 - propsys/IPropertySystem::RefreshPropertySchema
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.dll
api_name:
 - IPropertySystem.RefreshPropertySchema
---

# IPropertySystem::RefreshPropertySchema


## -description

Not supported.



## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Indicates schema files reloaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Indicates calling context does not have proper privileges.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a>

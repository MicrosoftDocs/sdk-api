---
UID: NF:wcmconfig.ISettingsItem.GetRestrictionFacets
title: ISettingsItem::GetRestrictionFacets
author: windows-sdk-content
description: Gets the restrictions defined for this item.
old-location: smi\isettingsitem_getrestrictionfacets.htm
old-project: SMI
ms.assetid: 64cf82d5-c210-4ff2-a7c8-1a284859382e
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetRestrictionFacets, GetRestrictionFacets method [SMI], GetRestrictionFacets method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetRestrictionFacets method, ISettingsItem.GetRestrictionFacets, ISettingsItem::GetRestrictionFacets, smi.isettingsitem_getrestrictionfacets, wcmconfig/ISettingsItem::GetRestrictionFacets
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsItem.GetRestrictionFacets
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsItem::GetRestrictionFacets


## -description


Gets the restrictions defined for this item.


## -parameters




### -param RestrictionFacets [out]

A bitmask of  the <a href="https://msdn.microsoft.com/b9e62904-f6a9-4299-a558-51b57bd7d3db">WcmRestrictionFacets</a> values that are defined for this item.


## -returns



This method can return one of these values.

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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item is not a scalar setting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there is no value for the item.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a>
 

 


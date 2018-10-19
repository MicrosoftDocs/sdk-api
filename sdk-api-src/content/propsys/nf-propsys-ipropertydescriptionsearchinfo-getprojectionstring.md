---
UID: NF:propsys.IPropertyDescriptionSearchInfo.GetProjectionString
title: IPropertyDescriptionSearchInfo::GetProjectionString
author: windows-sdk-content
description: Returns a pointer to a string containing the canonical name of the item.
old-location: properties\IPropertyDescriptionSearchInfo_GetProjectionString.htm
tech.root: properties
ms.assetid: 06881c29-fafb-47be-abdb-906e289ee5fc
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetProjectionString, GetProjectionString method [Windows Properties], GetProjectionString method [Windows Properties],IPropertyDescriptionSearchInfo interface, IPropertyDescriptionSearchInfo interface [Windows Properties],GetProjectionString method, IPropertyDescriptionSearchInfo.GetProjectionString, IPropertyDescriptionSearchInfo::GetProjectionString, _shell_IPropertyDescriptionSearchInfo_GetProjectionString, properties.IPropertyDescriptionSearchInfo_GetProjectionString, propsys/IPropertyDescriptionSearchInfo::GetProjectionString, shell.IPropertyDescriptionSearchInfo_GetProjectionString
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
 - IPropertyDescriptionSearchInfo.GetProjectionString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescriptionSearchInfo::GetProjectionString


## -description


Returns a pointer to a string containing the canonical name of the item.


## -parameters




### -param ppszProjection [out]

Type: <b>LPWSTR*</b>

When this method returns successfully, contains a pointer to a string containing the canonical name of the item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




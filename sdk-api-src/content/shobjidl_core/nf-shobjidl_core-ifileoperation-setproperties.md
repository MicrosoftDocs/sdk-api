---
UID: NF:shobjidl_core.IFileOperation.SetProperties
title: IFileOperation::SetProperties
author: windows-sdk-content
description: Declares a set of properties and values to be set on an item or items.
old-location: shell\IFileOperation_SetProperties.htm
tech.root: shell
ms.assetid: b54efc12-42e9-4a90-a4d9-0e75bcdba0d6
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFileOperation interface [Windows Shell],SetProperties method, IFileOperation.SetProperties, IFileOperation::SetProperties, SetProperties, SetProperties method [Windows Shell], SetProperties method [Windows Shell],IFileOperation interface, _shell_IFileOperation_SetProperties, shell.IFileOperation_SetProperties, shobjidl_core/IFileOperation::SetProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IFileOperation.SetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperation::SetProperties


## -description


Declares a set of properties and values to be set on an item or items.


## -parameters




### -param pproparray [in]

Type: <b><a href="https://msdn.microsoft.com/c7de40d0-9fe6-4c4b-ba17-c4648501ce0a">IPropertyChangeArray</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/c7de40d0-9fe6-4c4b-ba17-c4648501ce0a">IPropertyChangeArray</a>, which accesses a collection of <a href="https://msdn.microsoft.com/7bdc31d8-ba03-4010-8aa1-89701ebbf8cd">IPropertyChange</a> objects that specify the properties to be set and their new values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not set the new property values, it merely declares them. To set property values on an item or a group of items, you must make at least the sequence of calls detailed here:

                

<ol>
<li>Call <b>IFileOperation::SetProperties</b> to declare the specific properties to be set and their new values.</li>
<li>Call <a href="https://msdn.microsoft.com/35330c7c-29fc-4337-a538-863925398b0d">IFileOperation::ApplyPropertiesToItem</a> or <a href="https://msdn.microsoft.com/d24aa63e-99ef-470c-9723-e561ee0a56bc">IFileOperation::ApplyPropertiesToItems</a> to declare the item or items whose properties are to be set.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to apply the properties to the item or items.</li>
</ol>



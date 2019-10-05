---
UID: NF:shobjidl_core.IFileOperation.ApplyPropertiesToItems
title: IFileOperation::ApplyPropertiesToItems (shobjidl_core.h)
author: windows-sdk-content
description: Declares a set of items for which to apply a common set of property values.
old-location: shell\IFileOperation_ApplyPropertiesToItems.htm
tech.root: shell
ms.assetid: d24aa63e-99ef-470c-9723-e561ee0a56bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ApplyPropertiesToItems, ApplyPropertiesToItems method [Windows Shell], ApplyPropertiesToItems method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],ApplyPropertiesToItems method, IFileOperation.ApplyPropertiesToItems, IFileOperation::ApplyPropertiesToItems, _shell_IFileOperation_ApplyPropertiesToItems, shell.IFileOperation_ApplyPropertiesToItems, shobjidl_core/IFileOperation::ApplyPropertiesToItems
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IFileOperation.ApplyPropertiesToItems"
dev_langs:
 - c++
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
 - IFileOperation.ApplyPropertiesToItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileOperation::ApplyPropertiesToItems


## -description


Declares a set of items for which to apply a common set of property values.


## -parameters




### -param punkItems [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> object which represents the group of items.  You can also point to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist">IPersistIDList</a> object to represent a single item, effectively accomplishing the same function as <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-applypropertiestoitem">IFileOperation::ApplyPropertiesToItem</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not apply the properties to the items, it merely declares the items. To set property values on a group of items, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setproperties">IFileOperation::SetProperties</a> to declare the specific properties to be set and their new values.</li>
<li>Call <b>IFileOperation::ApplyPropertiesToItems</b> to declare the items whose property values are to be set.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to apply the properties to the items.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-applypropertiestoitem">IFileOperation::ApplyPropertiesToItem</a>
 

 


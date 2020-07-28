---
UID: NF:shobjidl_core.IDataObjectProvider.SetDataObject
title: IDataObjectProvider::SetDataObject (shobjidl_core.h)
description: Wraps an IDataObject instance as a Windows Runtime DataPackage.
helpviewer_keywords: ["IDataObjectProvider interface [Windows Shell]","SetDataObject method","IDataObjectProvider.SetDataObject","IDataObjectProvider::SetDataObject","SetDataObject","SetDataObject method [Windows Shell]","SetDataObject method [Windows Shell]","IDataObjectProvider interface","shell.IDataObjectProvider_SetDataObject","shobjidl_core/IDataObjectProvider::SetDataObject"]
old-location: shell\IDataObjectProvider_SetDataObject.htm
tech.root: shell
ms.assetid: 4A7787E5-8C16-4cd2-B46F-67F6F636989B
ms.date: 12/05/2018
ms.keywords: IDataObjectProvider interface [Windows Shell],SetDataObject method, IDataObjectProvider.SetDataObject, IDataObjectProvider::SetDataObject, SetDataObject, SetDataObject method [Windows Shell], SetDataObject method [Windows Shell],IDataObjectProvider interface, shell.IDataObjectProvider_SetDataObject, shobjidl_core/IDataObjectProvider::SetDataObject
f1_keywords:
- shobjidl_core/IDataObjectProvider.SetDataObject
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- IDataObjectProvider.SetDataObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataObjectProvider::SetDataObject


## -description


Wraps an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> instance as a Windows Runtime <a href="https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.datatransfer.datapackage.aspx">DataPackage</a>.


## -parameters




### -param dataObject [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface pointer to the data object from which to build the DataPackage object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idataobjectprovider">IDataObjectProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idataobjectprovider-getdataobject">IDataObjectProvider::GetDataObject</a>
 

 


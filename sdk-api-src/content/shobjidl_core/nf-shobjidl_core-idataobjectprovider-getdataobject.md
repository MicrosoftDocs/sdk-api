---
UID: NF:shobjidl_core.IDataObjectProvider.GetDataObject
title: IDataObjectProvider::GetDataObject (shobjidl_core.h)
description: Gets an IDataObject representation of the current DataPackage object.helpviewer_keywords: ["GetDataObject","GetDataObject method [Windows Shell]","GetDataObject method [Windows Shell]","IDataObjectProvider interface","IDataObjectProvider interface [Windows Shell]","GetDataObject method","IDataObjectProvider.GetDataObject","IDataObjectProvider::GetDataObject","shell.IDataObjectProvider_GetDataObject","shobjidl_core/IDataObjectProvider::GetDataObject"]
old-location: shell\IDataObjectProvider_GetDataObject.htm
tech.root: shell
ms.assetid: 7F3678B2-4B18-4344-ADEE-F0D0A6CE635E
ms.date: 12/05/2018
ms.keywords: GetDataObject, GetDataObject method [Windows Shell], GetDataObject method [Windows Shell],IDataObjectProvider interface, IDataObjectProvider interface [Windows Shell],GetDataObject method, IDataObjectProvider.GetDataObject, IDataObjectProvider::GetDataObject, shell.IDataObjectProvider_GetDataObject, shobjidl_core/IDataObjectProvider::GetDataObject
f1_keywords:
- shobjidl_core/IDataObjectProvider.GetDataObject
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
- IDataObjectProvider.GetDataObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataObjectProvider::GetDataObject


## -description


Gets an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> representation of the current <a href="https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.datatransfer.datapackage.aspx">DataPackage</a> object.


## -parameters




### -param dataObject [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>**</b>

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface pointer that, when this method returns successfully, points to the <b>IDataObject</b> representation of the <a href="https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.datatransfer.datapackage.aspx">DataPackage</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idataobjectprovider">IDataObjectProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idataobjectprovider-setdataobject">IDataObjectProvider::SetDataObject</a>
 

 


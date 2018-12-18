---
UID: NF:shobjidl_core.IDataObjectProvider.SetDataObject
title: IDataObjectProvider::SetDataObject
author: windows-sdk-content
description: Wraps an IDataObject instance as a Windows Runtime DataPackage.
old-location: shell\IDataObjectProvider_SetDataObject.htm
tech.root: shell
ms.assetid: 4A7787E5-8C16-4cd2-B46F-67F6F636989B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataObjectProvider interface [Windows Shell],SetDataObject method, IDataObjectProvider.SetDataObject, IDataObjectProvider::SetDataObject, SetDataObject, SetDataObject method [Windows Shell], SetDataObject method [Windows Shell],IDataObjectProvider interface, shell.IDataObjectProvider_SetDataObject, shobjidl_core/IDataObjectProvider::SetDataObject
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataObjectProvider::SetDataObject


## -description


Wraps an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> instance as a Windows Runtime <a href="http://go.microsoft.com/fwlink/p/?linkid=267543">DataPackage</a>.


## -parameters




### -param dataObject [in]

An <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface pointer to the data object from which to build the DataPackage object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/57A5003A-11DF-42c2-9C00-7DE35898B64D">IDataObjectProvider</a>



<a href="https://msdn.microsoft.com/7F3678B2-4B18-4344-ADEE-F0D0A6CE635E">IDataObjectProvider::GetDataObject</a>
 

 


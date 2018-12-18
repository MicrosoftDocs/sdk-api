---
UID: NF:shobjidl_core.IDataObjectProvider.GetDataObject
title: IDataObjectProvider::GetDataObject
author: windows-sdk-content
description: Gets an IDataObject representation of the current DataPackage object.
old-location: shell\IDataObjectProvider_GetDataObject.htm
tech.root: shell
ms.assetid: 7F3678B2-4B18-4344-ADEE-F0D0A6CE635E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDataObject, GetDataObject method [Windows Shell], GetDataObject method [Windows Shell],IDataObjectProvider interface, IDataObjectProvider interface [Windows Shell],GetDataObject method, IDataObjectProvider.GetDataObject, IDataObjectProvider::GetDataObject, shell.IDataObjectProvider_GetDataObject, shobjidl_core/IDataObjectProvider::GetDataObject
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
 - IDataObjectProvider.GetDataObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataObjectProvider::GetDataObject


## -description


Gets an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> representation of the current <a href="http://go.microsoft.com/fwlink/p/?linkid=267543">DataPackage</a> object.


## -parameters




### -param dataObject [out]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>**</b>

The address of an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface pointer that, when this method returns successfully, points to the <b>IDataObject</b> representation of the <a href="http://go.microsoft.com/fwlink/p/?linkid=267543">DataPackage</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/57A5003A-11DF-42c2-9C00-7DE35898B64D">IDataObjectProvider</a>



<a href="https://msdn.microsoft.com/4A7787E5-8C16-4cd2-B46F-67F6F636989B">IDataObjectProvider::SetDataObject</a>
 

 


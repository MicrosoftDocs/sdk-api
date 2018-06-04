---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAppxBundleFactory::CreateBundleWriter


## -description


Creates a write-only bundle object to which app packages can be added.  


## -parameters




### -param outputStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The output stream that receives the serialized package data. The stream must support at least the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a> method.


### -param bundleVersion [in]

Type: <b>UINT64</b>

The version number of the bundle.

 If set to 0, <b>CreateBundleWriter</b> sets the version number of the bundle to a value derived from the current system time.  We recommend passing 0 so version numbers are automatically generated and each successive call generates a higher version number.


For example, if you call <b>CreateBundleWriter</b> on 2013/12/23 3:45:00 AM UTC with <i>bundleVersion</i> set to 0, the version number of the bundle becomes 2013.1223.0345.0000.



### -param bundleWriter [out, retval]

Type: <b>IAppxBundleWriter**</b>

The bundle writer created by this method.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 




## -remarks



Content added to the bundle is serialized out as an Appx bundle file to <i>outputStream</i>. 




## -see-also




<a href="https://msdn.microsoft.com/33A320BD-7B68-4C42-A776-25CC744C6652">IAppxBundleFactory</a>
 

 


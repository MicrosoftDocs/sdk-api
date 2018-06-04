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

# IPortableDevice::Advise


## -description



        The <b>Advise</b> method registers an application-defined callback that receives device events.
      


## -parameters




### -param dwFlags [in]

<b>DWORD</b> that specifies option flags.
          


### -param pCallback [in]


            Pointer to a callback object.
          


### -param pParameters [in]


            This parameter is ignored and should be set to <b>NULL</b>.
          


### -param ppszCookie [out]


            A string that represents a unique context ID. This is used to unregister for callbacks when calling <a href="https://msdn.microsoft.com/6720e92b-35cd-4e3f-bd21-36337cf80140">Unadvise</a>.
          


## -returns




            The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The application-defined callback was successfully registered.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/529a8b7a-08b4-47de-8ed3-28e8fff0ede2">Handling Events from the Device</a>



<a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice Interface</a>
 

 


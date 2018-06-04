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

# ID3D11Device3::GetImmediateContext3


## -description



          Gets an immediate context, which can play back <a href="https://msdn.microsoft.com/4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e">command lists</a>.
        


## -parameters




### -param ppImmediateContext [out]

Type: <b><a href="https://msdn.microsoft.com/65F462DB-5546-4B23-B438-60067FD60103">ID3D11DeviceContext3</a>**</b>


            Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/65F462DB-5546-4B23-B438-60067FD60103">ID3D11DeviceContext3</a> interface pointer is initialized.
          


## -returns



This method does not return a value.




## -remarks




          The
          <b>GetImmediateContext3</b>
          method outputs an
          <a href="https://msdn.microsoft.com/65F462DB-5546-4B23-B438-60067FD60103">ID3D11DeviceContext3</a>
          object that represents an immediate context, which is used to perform rendering that you want immediately submitted to a device.
          For most apps, an immediate context is the primary object that is used to draw your scene.
        


          The <b>GetImmediateContext3</b> method increments the reference count of the immediate context by one.
          Therefore, you must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the returned interface pointer when you are done with it to avoid a memory leak.
        




## -see-also




<a href="https://msdn.microsoft.com/E66CDC7E-21B5-4675-A7A1-6F94940A4C13">ID3D11Device1::GetImmediateContext1</a>



<a href="https://msdn.microsoft.com/3DCA642D-7992-4C1E-8AD2-CA0099188A46">ID3D11Device2::GetImmediateContext2</a>



<a href="https://msdn.microsoft.com/0AA10851-0077-4075-BD41-72FCD7BC0556">ID3D11Device3</a>



<a href="https://msdn.microsoft.com/0349f0b8-7696-4d72-bed4-d39b9ac90f6c">ID3D11Device::GetImmediateContext</a>
 

 


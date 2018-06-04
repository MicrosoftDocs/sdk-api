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

# ID3D11Device::CreateDeferredContext


## -description



      Creates a deferred context, which can record command lists.


## -parameters




### -param ContextFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Reserved for future use.
            Pass 0.
          


### -param ppDeferredContext [out, optional]

Type: <b><a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>**</b>


            Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> interface pointer is initialized.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


              Returns S_OK if successful; otherwise, returns one of the following:
            

<ul>
<li>
                Returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if the video card has been physically removed from the system, or a driver upgrade for the video card has occurred.
                If this error occurs, you should destroy and recreate the device.
              </li>
<li>
                Returns <b>DXGI_ERROR_INVALID_CALL</b> if the <b>CreateDeferredContext</b> method cannot be called from the current context.
                For example, if the device was created with the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value,  <b>CreateDeferredContext</b> returns <b>DXGI_ERROR_INVALID_CALL</b>.
              </li>
<li>
                Returns <b>E_INVALIDARG</b> if the <i>ContextFlags</i> parameter is invalid.
              </li>
<li>
                Returns <b>E_OUTOFMEMORY</b> if the application has exhausted available memory.
              </li>
</ul>



## -remarks




          A deferred context is a thread-safe context that you can use to record graphics commands on a thread other than the main rendering thread.
          Using a deferred context, you can record graphics commands into a command list that is encapsulated by the <a href="https://msdn.microsoft.com/432f1d21-bf13-4569-9c8f-04f5d2845150">ID3D11CommandList</a> interface.
          After all scene items are recorded, you can then submit them to the main render thread for final rendering.
          In this manner, you can perform rendering tasks concurrently across multiple threads and potentially improve performance in multi-core CPU scenarios.
        


          You can create multiple deferred contexts.
        

<div class="alert"><b>Note</b>  
          If you use the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value to create the device that is represented by <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>, the <b>CreateDeferredContext</b> method will fail, and you will not be able to create a deferred context.
        </div>
<div> </div>

          For more information about deferred contexts, see <a href="https://msdn.microsoft.com/8991be9f-c882-4752-9048-704fe4ae1725">Immediate and Deferred Rendering</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>



<a href="https://msdn.microsoft.com/2F7E343F-2A25-44F2-9352-5F378718D6F6">ID3D11Device1::CreateDeferredContext1</a>



<a href="https://msdn.microsoft.com/57901FAC-428C-437B-9C9B-2DB2D16049F8">ID3D11Device2::CreateDeferredContext2</a>



<a href="https://msdn.microsoft.com/78B52E38-3256-4151-96DA-4C81A2A516CF">ID3D11Device3::CreateDeferredContext3</a>
 

 


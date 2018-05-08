---
UID: NF:d3d11_1.ID3D11Device1.CreateDeferredContext1
title: ID3D11Device1::CreateDeferredContext1
author: windows-driver-content
description: Creates a deferred context, which can record command lists.
old-location: direct3d11\id3d11device1_createdeferredcontext1.htm
old-project: direct3d11
ms.assetid: 2F7E343F-2A25-44F2-9352-5F378718D6F6
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: CreateDeferredContext1, CreateDeferredContext1 method [Direct3D 11], CreateDeferredContext1 method [Direct3D 11],ID3D11Device1 interface, ID3D11Device1 interface [Direct3D 11],CreateDeferredContext1 method, ID3D11Device1.CreateDeferredContext1, ID3D11Device1::CreateDeferredContext1, d3d11_1/ID3D11Device1::CreateDeferredContext1, direct3d11.id3d11device1_createdeferredcontext1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Device1.CreateDeferredContext1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device1::CreateDeferredContext1


## -description



      Creates a deferred context, which can record command lists.


## -parameters




### -param ContextFlags


            Reserved for future use.
            Pass 0.
          


### -param ppDeferredContext [out, optional]


            Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a> interface pointer is initialized.
          


## -returns




              Returns S_OK if successful; otherwise, returns one of the following:
            

<ul>
<li>
                Returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if the graphics adapter has been physically removed from the computer or a driver upgrade for the graphics adapter has occurred.
                If this error occurs, you should destroy and re-create the device.
              </li>
<li>
                Returns <b>DXGI_ERROR_INVALID_CALL</b> if the <b>CreateDeferredContext1</b> method cannot be called from the current context.
                For example, if the device was created with the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value,  <b>CreateDeferredContext1</b> returns <b>DXGI_ERROR_INVALID_CALL</b>.
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
          By using a deferred context, you can record graphics commands into a command list that is encapsulated by the <a href="https://msdn.microsoft.com/432f1d21-bf13-4569-9c8f-04f5d2845150">ID3D11CommandList</a> interface.
          After you record all scene items, you can then submit them to the main render thread for final rendering.
          In this manner, you can perform rendering tasks concurrently across multiple threads and potentially improve performance in multi-core CPU scenarios.
        


          You can create multiple deferred contexts.
        

<div class="alert"><b>Note</b>  
          If you use the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value to create the device that is represented by <a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a>, the <b>CreateDeferredContext1</b> method will fail, and you will not be able to create a deferred context.
        </div>
<div> </div>

          For more information about deferred contexts, see <a href="https://msdn.microsoft.com/8991be9f-c882-4752-9048-704fe4ae1725">Immediate and Deferred Rendering</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a>



<a href="https://msdn.microsoft.com/57901FAC-428C-437B-9C9B-2DB2D16049F8">ID3D11Device2::CreateDeferredContext2</a>



<a href="https://msdn.microsoft.com/78B52E38-3256-4151-96DA-4C81A2A516CF">ID3D11Device3::CreateDeferredContext3</a>



<a href="https://msdn.microsoft.com/fbf01844-eaf1-4360-833e-c95ba686fff5">ID3D11Device::CreateDeferredContext</a>
 

 


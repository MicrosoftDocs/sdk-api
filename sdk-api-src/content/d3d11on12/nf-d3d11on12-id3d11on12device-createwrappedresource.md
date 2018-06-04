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

# ID3D11On12Device::CreateWrappedResource


## -description



          This method creates D3D11 resources for use with D3D 11on12.
        


## -parameters




### -param pResource12 [in]

Type: <b>IUnknown*</b>


            A pointer to an already-created D3D12 resource or heap.
          


### -param pFlags11 [in]

Type: <b>const <a href="https://msdn.microsoft.com/50C1ACA1-714C-467A-A548-B5EE50DA3E3D">D3D11_RESOURCE_FLAGS</a>*</b>


              A <a href="https://msdn.microsoft.com/50C1ACA1-714C-467A-A548-B5EE50DA3E3D">D3D11_RESOURCE_FLAGS</a> structure that enables an application to override flags that would be inferred by the resource/heap properties.
              The D3D11_RESOURCE_FLAGS structure contains bind flags, misc flags, and CPU access flags.
            


### -param InState

Type: <b><a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a></b>


            The use of the resource on input, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> enumeration constants.
          


### -param OutState

Type: <b><a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a></b>


            The use of the resource on output, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> enumeration constants.
          


### -param riid

Type: <b>REFIID</b>


            The globally unique identifier (<b>GUID</b>) for the wrapped resource interface.
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the wrapped resource can be obtained by using the __uuidof() macro.
            For example, __uuidof(<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>) will get the <b>GUID</b> of the interface to a wrapped resource.
          


### -param ppResource11 [out, optional]

Type: <b>void**</b>


            After the method returns, points to the newly created wrapped D3D11 resource or heap.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/031F9AC2-E5C0-47F9-B084-2D2431F1187A">ID3D11On12Device</a>
 

 


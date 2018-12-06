---
UID: NS:comsvcs.__MIDL___MIDL_itf_autosvcs_0000_0013_0001
title: "__MIDL___MIDL_itf_autosvcs_0000_0013_0001"
author: windows-sdk-content
description: Represents contextual information about an event, such as the time it was generated and which process server and COM+ application generated it.
old-location: cos\comsvcseventinfo.htm
tech.root: cossdk
ms.assetid: f4aa0892-4c93-42ea-adc6-1b304b917389
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: COMSVCSEVENTINFO, COMSVCSEVENTINFO structure [COM+], __MIDL___MIDL_itf_autosvcs_0000_0013_0001, _dtc_Event_Structure, comsvcs/COMSVCSEVENTINFO, cos.comsvcseventinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - COMSVCSEVENTINFO
product: Windows
targetos: Windows
req.typenames: COMSVCSEVENTINFO
req.redist: 
---

# __MIDL___MIDL_itf_autosvcs_0000_0013_0001 structure


## -description


Represents contextual information about an event, such as the time it was generated and which process server and COM+ application generated it.


## -struct-fields




### -field cbSize

The size of this structure, in bytes.


### -field dwPid

The process ID of the server application from which the event originated.


### -field lTime

The coordinated universal time of the event, as seconds elapsed since midnight, January 1, 1970.


### -field lMicroTime

The microseconds added to <b>lTime</b> for time to microsecond resolution.


### -field perfCount

The value of the high-resolution performance counter when the event originated.


### -field guidApp

The applications globally unique identifier (GUID) for the first component instantiated in <b>dwPid</b>. If you are subscribing to an administration interface or event and the event is not generated from a COM+ application, this member is set to zero.


### -field sMachineName

The fully qualified name of the computer where the event originated.


## -see-also




<a href="https://msdn.microsoft.com/9b702bcd-d5a6-41fa-98ce-00a245dfe770">IComActivityEvents</a>



<a href="https://msdn.microsoft.com/45e0d26b-7485-436b-9b64-fa48217b32d1">IComApp2Events</a>



<a href="https://msdn.microsoft.com/61ae1926-601b-4d97-80e4-d2d2098ced39">IComAppEvents</a>



<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>



<a href="https://msdn.microsoft.com/e484cad0-3b7e-4822-bbde-c953cb0301ca">IComExceptionEvents</a>



<a href="https://msdn.microsoft.com/f064a5cd-c84d-4b80-96fc-1036af333901">IComIdentityEvents</a>



<a href="https://msdn.microsoft.com/2fb2904d-7069-4303-bb3c-2caef9499c1e">IComInstance2Events</a>



<a href="https://msdn.microsoft.com/11e4559e-04c5-4fa9-b618-458ca7daf00e">IComInstanceEvents</a>



<a href="https://msdn.microsoft.com/8be6dddb-ed57-4715-8933-8a0e478095c8">IComLTxEvents</a>



<a href="https://msdn.microsoft.com/e0642cb2-d5f2-4e4b-ad35-7818983ed467">IComMethod2Events</a>



<a href="https://msdn.microsoft.com/24670a23-4300-48f9-a089-dff3082cb544">IComMethodEvents</a>



<a href="https://msdn.microsoft.com/976b8c1a-5ccd-48e2-a77c-10d4de9a4ffa">IComObjectConstruction2Events</a>



<a href="https://msdn.microsoft.com/c5fdb9b1-937e-43cb-93ff-e90f8c268fee">IComObjectConstructionEvents</a>



<a href="https://msdn.microsoft.com/4354fc5b-4d72-4a56-b246-2ae2cf9b5ae1">IComObjectEvents</a>



<a href="https://msdn.microsoft.com/2aac494d-52ce-408c-8444-8792b5b53604">IComObjectPool2Events</a>



<a href="https://msdn.microsoft.com/a830b40b-a1b1-464e-b532-91cebd4e5d2f">IComObjectPoolEvents</a>



<a href="https://msdn.microsoft.com/f1891d8b-e3d0-4378-ac67-c2c0ddd65602">IComObjectPoolEvents2</a>



<a href="https://msdn.microsoft.com/d7c8220d-a302-4f95-b0b6-8d47f9f27da7">IComQCEvents</a>



<a href="https://msdn.microsoft.com/fdc664b6-0459-4cbd-8e9e-0c3fe82e4321">IComResourceEvents</a>



<a href="https://msdn.microsoft.com/83366f18-8dd4-4c3d-8362-4fbcc4c33b95">IComSecurityEvents</a>



<a href="https://msdn.microsoft.com/a6523088-cca4-41c1-a3fe-d8cb7320ff33">IComThreadEvents</a>



<a href="https://msdn.microsoft.com/bed709ca-5083-4073-a9f9-2b7b7f14cf87">IComTrackingInfoEvents</a>



<a href="https://msdn.microsoft.com/103776c8-1cdc-46a5-a2ce-54163726e602">IComTransaction2Events</a>



<a href="https://msdn.microsoft.com/f28a0ef5-1c9a-4fdc-bb10-2c381f22f5e3">IComTransactionEvents</a>



<a href="https://msdn.microsoft.com/a443b54a-018f-48a0-b61c-9e18e9567a22">IComUserEvent</a>
 

 


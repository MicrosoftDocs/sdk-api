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

# ISurrogate::LoadDllServer


## -description


Loads a DLL server into the implementing surrogate. COM calls this method when there is an activation request for the DLL server's class, if the class is registered as <a href="https://msdn.microsoft.com/ae02d828-9cdb-4faa-8fa9-971da97e27b1">DllSurrogate</a>.




## -parameters




### -param Clsid [in]

The CLSID of the DLL server to be loaded.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -remarks



Upon receiving a load request through <b>LoadDllServer</b>, the surrogate must perform the following steps:

<ol>
<li>Create a class factory object that supports <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, <a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a>, and <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>.</li>
<li>Call <a href="https://msdn.microsoft.com/d27bfa6c-194a-41f1-8fcf-76c4dff14a8a">CoRegisterClassObject</a> to register the new class factory object as the class factory for the requested CLSID.</li>
</ol>
This class factory's implementation of <a href="https://msdn.microsoft.com/45d34150-9e0b-4a76-a784-c81434ec73b8">IClassFactory::CreateInstance</a> will create an instance of the requested CLSID method by calling <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a> to get the class factory which creates an actual object for the given CLSID.




## -see-also




<a href="https://msdn.microsoft.com/4d1c6ca6-ab21-429c-9433-7c95d9e757b5">CoRegisterSurrogate</a>



<a href="https://msdn.microsoft.com/ae02d828-9cdb-4faa-8fa9-971da97e27b1">DllSurrogate</a>



<a href="https://msdn.microsoft.com/fbed0514-3646-4744-aa7a-4a98f1a12cc0">ISurrogate</a>



<a href="https://msdn.microsoft.com/510e38e5-1965-46f4-b09c-6fa585cff993">Writing a Custom Surrogate</a>
 

 


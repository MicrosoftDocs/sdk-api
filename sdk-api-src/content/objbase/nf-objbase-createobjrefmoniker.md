---
UID: NF:objbase.CreateObjrefMoniker
title: CreateObjrefMoniker function
author: windows-sdk-content
description: Creates an OBJREF moniker based on a pointer to an object.
old-location: com\createobjrefmoniker.htm
old-project: com
ms.assetid: 0a214a11-776c-4ef6-af68-a141398f853c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CreateObjrefMoniker, CreateObjrefMoniker function [COM], _com_CreateObjrefMoniker, com.createobjrefmoniker, objbase/CreateObjrefMoniker
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COMSD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
api_name:
-	CreateObjrefMoniker
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CreateObjrefMoniker function


## -description


Creates an OBJREF moniker based on a pointer to an object.


## -parameters




### -param punk [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the object that the moniker is to represent.


### -param ppmk [out]

Address of a pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on the OBJREF moniker that was created.


## -returns



This function can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -remarks



Clients use OBJREF monikers to obtain a marshaled pointer to a running object in the servers address space.

The server typically calls <b>CreateObjrefMoniker</b> to create an OBJREF moniker and then calls <a href="https://msdn.microsoft.com/424036c9-c097-4507-b562-4a01f9199b1f">IMoniker::GetDisplayName</a>, and finally releases the moniker. The display name for an OBJREF moniker is of the form:



OBJREF:<i>nnnnnnnn</i>

Where <i>nnnnnnnn</i> is an arbitrarily long base-64 encoding that encapsulates the computer location, process endpoint, and interface pointer ID (IPID) of the running object

The display name can then be transferred to the client as text. For example, the display name can reside on an HTML page that the client downloads. 

The client can pass the display name to <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a>, which creates an OBJREF moniker based on the display name. A call to the monikers <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> method then obtains a marshaled pointer to the running instance on the server.

For example, a server-side COM component contained in an Active Server Page can create an OBJREF moniker, obtain its display name, and write the display name to the HTML output that is sent to the client browser. A script that runs on the client side can use the display name to get access to the running object itself. A client-side Visual Basic script, for instance, could store the display name in a variable called strMyName and include this line:

<code>objMyInstance = GetObject(strMyName)</code>

The script engine internally makes the calls to <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> and <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a>, and the script can then use objMyInstance to refer directly to the running object.





## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 


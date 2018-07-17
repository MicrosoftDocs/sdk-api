---
UID: NF:ole2.OleLoad
title: OleLoad function
author: windows-sdk-content
description: Loads into memory an object nested within a specified storage object.
old-location: com\oleload.htm
old-project: com
ms.assetid: f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: OleLoad, OleLoad function [COM], _ole_OleLoad, com.oleload, ole2/OleLoad
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleLoad
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleLoad function


## -description


Loads into memory an object nested within a specified storage object.


## -parameters




### -param pStg [in]

Pointer to the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object from which to load the specified object.


### -param riid [in]

Reference to the identifier of the interface that the caller wants to use to communicate with the object after it is loaded.


### -param pClientSite [in]

Pointer to the <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a> interface on the client site object being loaded.


### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly loaded object.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified interface.

</td>
</tr>
</table>
 

Additionally, this function can return any of the error values returned by the <a href="https://msdn.microsoft.com/34379b8d-4e00-49cd-9fd1-65f88746c61a">IPersistStorage::Load</a> method.




## -remarks



OLE containers load objects into memory by calling this function. When calling the <b>OleLoad</b> function, the container application passes in a pointer to the open storage object in which the nested object is stored. Typically, the nested object to be loaded is a child storage object to the container's root storage object. Using the OLE information stored with the object, the object handler (usually, the default handler) attempts to load the object. On completion of the <b>OleLoad</b> function, the object is said to be in the loaded state with its object application not running.

Some applications load all of the object's native data. Containers often defer loading the contained objects until required to do so. For example, until an object is scrolled into view and needs to be drawn, it does not need to be loaded.

The <b>OleLoad</b> function performs the following steps:

<ul>
<li>If necessary, performs an automatic conversion of the object (see the <a href="https://msdn.microsoft.com/fe470f8a-b2f0-48a4-a270-77420bd1472a">OleDoAutoConvert</a> function).</li>
<li>Gets the CLSID from the open storage object by calling the <a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a> method.</li>
<li> Calls the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function to create an instance of the handler. If the handler code is not available, the default handler is used (see the <a href="https://msdn.microsoft.com/ffe87012-b000-4ed7-b0b2-78ffdc794d3b">OleCreateDefaultHandler</a> function).</li>
<li>Calls the <a href="https://msdn.microsoft.com/6690b5a3-bada-496c-89cb-a9ae1fc9dfb0">IOleObject::SetClientSite</a> method with the <i>pClientSite</i> parameter to inform the object of its client site.</li>
<li>Calls the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method for the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> interface. If successful, the <a href="https://msdn.microsoft.com/34379b8d-4e00-49cd-9fd1-65f88746c61a">IPersistStorage::Load</a> method is invoked for the object.</li>
<li>Queries and returns the interface identified by the <i>riid</i> parameter.</li>
</ul>



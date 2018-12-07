---
UID: NF:objidl.IGlobalInterfaceTable.GetInterfaceFromGlobal
title: IGlobalInterfaceTable::GetInterfaceFromGlobal
author: windows-sdk-content
description: Retrieves a pointer to an interface on an object that is usable by the calling apartment. This interface must be currently registered in the global interface table.
old-location: com\iglobalinterfacetable_getinterfacefromglobal.htm
tech.root: com
ms.assetid: 3b37184d-c4e8-47b2-8f3f-008d3ea00759
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInterfaceFromGlobal, GetInterfaceFromGlobal method [COM], GetInterfaceFromGlobal method [COM],IGlobalInterfaceTable interface, IGlobalInterfaceTable interface [COM],GetInterfaceFromGlobal method, IGlobalInterfaceTable.GetInterfaceFromGlobal, IGlobalInterfaceTable::GetInterfaceFromGlobal, _com_iglobalinterfacetable_getinterfacefromglobal, com.iglobalinterfacetable_getinterfacefromglobal, objidlbase/IGlobalInterfaceTable::GetInterfaceFromGlobal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - COM
api_location:
 - objidlbase.h
api_name:
 - IGlobalInterfaceTable.GetInterfaceFromGlobal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGlobalInterfaceTable::GetInterfaceFromGlobal


## -description


Retrieves a pointer to an interface on an object that is usable by the calling apartment. This interface must be currently registered in the global interface table.


## -parameters




### -param dwCookie [in]

Identifies the interface (and its object), and is retrieved through a call to <a href="https://msdn.microsoft.com/5282b0b8-4eab-4114-8061-6d74db3756b7">IGlobalInterfaceTable::RegisterInterfaceInGlobal</a>.


### -param riid [in]

The IID of the interface.


### -param ppv [out]

A pointer to the pointer for the requested interface.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



After an interface has been registered in the global interface table, an apartment can get a pointer to this interface by calling the <b>GetInterfaceFromGlobal</b> method with the supplied cookie. This pointer to the interface can be used in the calling apartment but not by other apartments in the process.

The application is responsible for coordinating access to the global variable during calls to <a href="https://msdn.microsoft.com/202bf33a-5827-4cbf-b977-86167a9c633f">IGlobalInterfaceTable::RevokeInterfaceFromGlobal</a>. That is, the application should ensure that one thread does not call <b>RevokeInterfaceFromGlobal</b> while another thread is calling <b>GetInterfaceFromGlobal</b> with the same cookie. Multiple calls to <b>GetInterfaceFromGlobal</b> for the same cookie are permitted.

The <b>GetInterfaceFromGlobal</b> method calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the pointer obtained in the <i>ppv</i> parameter. It is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on this pointer.




## -see-also




<a href="https://msdn.microsoft.com/0c1feee7-e33b-4b5d-8e35-4de6895e3947">IGlobalInterfaceTable</a>
 

 


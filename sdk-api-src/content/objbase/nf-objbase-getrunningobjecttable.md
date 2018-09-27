---
UID: NF:objbase.GetRunningObjectTable
title: GetRunningObjectTable function
author: windows-sdk-content
description: Returns a pointer to the IRunningObjectTable interface on the local running object table (ROT).
old-location: com\getrunningobjecttable.htm
tech.root: com
ms.assetid: 65d9cf7d-cc8a-4199-9a4a-7fd67ef8872d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRunningObjectTable, GetRunningObjectTable function [COM], _com_GetRunningObjectTable, com.getrunningobjecttable, objbase/GetRunningObjectTable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - GetRunningObjectTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetRunningObjectTable function


## -description


Returns a pointer to the <a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a> interface on the local running object table (ROT).


## -parameters




### -param reserved [in]

This parameter is reserved and must be 0.


### -param pprot [out]

The address of an <a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>* pointer variable that receives the interface pointer to the local ROT. When the function is successful, the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the interface pointer. If an error occurs, *<i>pprot</i> is undefined. 


## -returns



This function can return the standard return values E_UNEXPECTED and S_OK.




## -remarks



Each workstation has a local ROT that maintains a table of the objects that have been registered as running on that computer. This function returns an <a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a> interface pointer, which provides access to that table.

Moniker providers, which hand out monikers that identify objects so they are accessible to others, should call <b>GetRunningObjectTable</b>. Use the interface pointer returned by this function to register your objects when they begin running, to record the times that those objects are modified, and to revoke their registrations when they stop running. See the <a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a> interface for more information.



Compound-document link sources are the most common example of moniker providers. These include server applications that support linking to their documents (or portions of a document) and container applications that support linking to embeddings within their documents. Server applications that do not support linking can also use the ROT to cooperate with container applications that support linking to embeddings.

If you are implementing the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface to write a new moniker class, and you need an interface pointer to the ROT, call <a href="https://msdn.microsoft.com/26938d07-d772-4e72-a6aa-57dd2f2cece1">IBindCtx::GetRunningObjectTable</a> rather than the <b>GetRunningObjectTable</b> function. This allows future implementations of the <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface to modify binding behavior.




## -see-also




<a href="https://msdn.microsoft.com/26938d07-d772-4e72-a6aa-57dd2f2cece1">IBindCtx::GetRunningObjectTable</a>



<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>
 

 


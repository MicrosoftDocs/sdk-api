---
UID: NF:objbase.CoRegisterMessageFilter
title: CoRegisterMessageFilter function
author: windows-sdk-content
description: Registers with OLE the instance of an IMessageFilter interface, which is to be used for handling concurrency issues on the current thread.
old-location: com\coregistermessagefilter.htm
old-project: com
ms.assetid: caa5b277-ddbd-4ba9-892d-590d953b8433
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CoRegisterMessageFilter, CoRegisterMessageFilter function [COM], _com_CoRegisterMessageFilter, com.coregistermessagefilter, objbase/CoRegisterMessageFilter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: COMSD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-private-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
 - API-MS-Win-Core-COM-Private-l1-1-1.dll
api_name:
 - CoRegisterMessageFilter
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CoRegisterMessageFilter function


## -description


Registers with OLE the instance of an <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a> interface, which is to be used for handling concurrency issues on the current thread. Only one message filter can be registered for each thread. Threads in multithreaded apartments cannot have message filters.


## -parameters




### -param lpMessageFilter [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a> interface on the message filter. This message filter should be registered on the current thread, replacing the previous message filter (if any). This parameter can be <b>NULL</b>, indicating that no message filter should be registered on the current thread.

Note that this function calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the interface pointer to the message filter.


### -param lplpMessageFilter [out, optional]

Address of the <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a>* pointer variable that receives the interface pointer to the previously registered message filter. If there was no previously registered message filter for the current thread, the value of *<i>lplpMessageFilter</i> is <b>NULL</b>.


## -returns



If the instance was registered or revoked successfully, the return value is S_OK; otherwise, it is S_FALSE.




## -remarks



To revoke the registered message filter, pass the previous message filter (possibly <b>NULL</b>) as the <i>lpMessageFilter</i> parameter to <b>CoRegisterMessageFilter</b>.





## -see-also




<a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a>
 

 


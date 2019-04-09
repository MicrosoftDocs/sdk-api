---
UID: NF:objidl.IDataAdviseHolder.SendOnDataChange
title: IDataAdviseHolder::SendOnDataChange (objidl.h)
author: windows-sdk-content
description: Sends notifications to each advise sink for which there is a connection established by calling the IAdviseSink::OnDataChange method for each advise sink currently being handled by this instance of the advise holder object.
old-location: com\idataadviseholder_sendondatachange.htm
tech.root: com
ms.assetid: b7385116-2ec7-4e12-a2dc-c9029a38d8fd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDataAdviseHolder interface [COM],SendOnDataChange method, IDataAdviseHolder.SendOnDataChange, IDataAdviseHolder::SendOnDataChange, SendOnDataChange, SendOnDataChange method [COM], SendOnDataChange method [COM],IDataAdviseHolder interface, _ole_idataadviseholder_sendondatachange, com.idataadviseholder_sendondatachange, objidl/IDataAdviseHolder::SendOnDataChange
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ObjIdl.h
api_name:
 - IDataAdviseHolder.SendOnDataChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataAdviseHolder::SendOnDataChange


## -description


Sends notifications to each advise sink for which there is a connection established by calling the <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a> method for each advise sink currently being handled by this instance of the advise holder object.


## -parameters




### -param pDataObject [in]

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object in which the data has just changed. This pointer is used in subsequent calls to <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a>.


### -param dwReserved [in]

This parameter is reserved and must be 0.


### -param advf [in]

Container for advise flags that specify how the call to <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a> is made. These flag values are from the enumeration <a href="https://msdn.microsoft.com/e1ad9c17-e492-4891-bf1d-cbac48ce537a">ADVF</a>. Typically, the value for <i>advf</i> is <b>NULL</b>. The only exception occurs when the data object is shutting down and must send a final notification that includes the actual data to sinks that have specified ADVF_DATAONSTOP and ADVF_NODATA in their call to <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>. In this case, <i>advf</i> contains ADVF_DATAONSTOP.


## -returns



This method returns S_OK on success.




## -remarks



The data object must call this method when it detects a change that would be of interest to an advise sink that has previously requested notification.

Most notifications include the actual data with them. The only exception is if the ADVF_NODATA flag was previously specified when the connection was initially set up in the <a href="https://msdn.microsoft.com/3b72a50b-a18f-4ec0-9d1d-52b07eb84faf">IDataAdviseHolder::Advise</a> method.

Before calling the <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a> method for each advise sink, this method obtains the actual data by calling the <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> method through the pointer specified in the <i>pDataObject</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a>



<a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a>
 

 


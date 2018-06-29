---
UID: NF:objidl.IDataAdviseHolder.Advise
title: IDataAdviseHolder::Advise
author: windows-sdk-content
description: Creates a connection between an advise sink and a data object for receiving notifications.
old-location: com\idataadviseholder_advise.htm
old-project: com
ms.assetid: 3b72a50b-a18f-4ec0-9d1d-52b07eb84faf
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ADVF_DATAONSTOP, ADVF_NODATA, ADVF_ONLYONCE, ADVF_PRIMEFIRST, Advise, Advise method [COM], Advise method [COM],IDataAdviseHolder interface, IDataAdviseHolder interface [COM],Advise method, IDataAdviseHolder.Advise, IDataAdviseHolder::Advise, _ole_idataadviseholder_advise, com.idataadviseholder_advise, objidl/IDataAdviseHolder::Advise
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IDataAdviseHolder.Advise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IDataAdviseHolder::Advise


## -description


Creates a connection between an advise sink and a data object for receiving notifications.




## -parameters




### -param pDataObject [in]

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object for which notifications are requested. If data in this object changes, a notification is sent to the advise sinks that have requested notification.


### -param pFetc [in]

A pointer to a <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure that contains the specified format, medium, and target device that is of interest to the advise sink requesting notification. For example, one sink may want to know only when the bitmap representation of the data in the data object changes. Another sink may be interested in only the metafile format of the same object. Each advise sink is notified when the data of interest changes. This data is passed back to the advise sink when notification occurs.


### -param advf [in]

A group of flags that  control the advisory connection. Possible values are from the <a href="https://msdn.microsoft.com/e1ad9c17-e492-4891-bf1d-cbac48ce537a">ADVF</a> enumeration. However, only some of the possible <b>ADVF</b> values are relevant for this method. The following table briefly describes the relevant values; a more detailed description can be found in the description of the <b>ADVF</b> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADVF_NODATA"></a><a id="advf_nodata"></a><dl>
<dt><b>ADVF_NODATA</b></dt>
</dl>
</td>
<td width="60%">
Asks that no data be sent along with the notification.

</td>
</tr>
<tr>
<td width="40%"><a id="ADVF_ONLYONCE"></a><a id="advf_onlyonce"></a><dl>
<dt><b>ADVF_ONLYONCE</b></dt>
</dl>
</td>
<td width="60%">
Causes the advisory connection to be destroyed after the first notification is sent. An implicit call to <a href="https://msdn.microsoft.com/baeb29fd-1dd2-4320-911d-b271b2250184">IDataAdviseHolder::Unadvise</a> is made on behalf of the caller to remove the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="ADVF_PRIMEFIRST"></a><a id="advf_primefirst"></a><dl>
<dt><b>ADVF_PRIMEFIRST</b></dt>
</dl>
</td>
<td width="60%">
Causes an initial notification to be sent regardless of whether data has changed from its current state.

</td>
</tr>
<tr>
<td width="40%"><a id="ADVF_DATAONSTOP"></a><a id="advf_dataonstop"></a><dl>
<dt><b>ADVF_DATAONSTOP</b></dt>
</dl>
</td>
<td width="60%">
When specified with ADVF_NODATA, this flag causes a last notification with the data included to be sent before the data object is destroyed. When ADVF_NODATA is not specified, this flag has no effect.

</td>
</tr>
</table>
 


### -param pAdvise [in]

A pointer to the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface on the advisory sink that receives the change notification.


### -param pdwConnection [out]

A pointer to a variable that receives a  token that identifies this connection. The calling object can later delete the advisory connection by passing this token to <a href="https://msdn.microsoft.com/baeb29fd-1dd2-4320-911d-b271b2250184">IDataAdviseHolder::Unadvise</a>. If this value is zero, the connection was not established.


## -returns



This method returns S_OK on success.




## -remarks



Through the connection established through this method, the advisory sink can receive future notifications in a call to <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a>.

An object issues a call to <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a> to request notification on changes to the format, medium, or target device of interest. This data is specified in the <i>pFormatetc</i> parameter. The <b>DAdvise</b> method is usually implemented to call <b>IDataAdviseHolder::Advise</b> to delegate the task of setting up and tracking a connection to the advise holder. When the format, medium, or target device in question changes, the data object calls <a href="https://msdn.microsoft.com/b7385116-2ec7-4e12-a2dc-c9029a38d8fd">IDataAdviseHolder::SendOnDataChange</a> to send the necessary notifications.



The established connection can be deleted by passing the value in <i>pdwConnection</i> in a call to <a href="https://msdn.microsoft.com/baeb29fd-1dd2-4320-911d-b271b2250184">IDataAdviseHolder::Unadvise</a>.




## -see-also




<a href="https://msdn.microsoft.com/a2114f2f-106a-4a26-ba94-1b40af90a0f3">CreateDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>
 

 


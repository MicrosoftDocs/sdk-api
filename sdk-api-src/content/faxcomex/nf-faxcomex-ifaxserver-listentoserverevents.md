---
UID: NF:faxcomex.IFaxServer.ListenToServerEvents
title: IFaxServer::ListenToServerEvents
author: windows-sdk-content
description: The IFaxServer::ListenToServerEvents method registers the FaxServer object to receive notifications about one or more types of server events, or to stop these notifications.
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_listentoserverevents_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8kmr.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxServer interface [Fax Service],ListenToServerEvents method, IFaxServer.ListenToServerEvents, IFaxServer::ListenToServerEvents, ListenToServerEvents, ListenToServerEvents method [Fax Service], ListenToServerEvents method [Fax Service],IFaxServer interface, _mfax_faxserver.listentoserverevents, fax._mfax_faxserver_cpp_mfax_faxserver_listentoserverevents_cpp, fax._mfax_faxserver_listentoserverevents, faxcomex/IFaxServer::ListenToServerEvents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxServer.ListenToServerEvents
 - IFaxServer.ListenToServerEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxServer.ListenToServerEvents
: 
---

# IFaxServer::ListenToServerEvents


## -description


The <b>IFaxServer::ListenToServerEvents</b> method registers the <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object to receive notifications about one or more types of server events, or to stop these notifications. 


## -parameters




### -param EventTypes [in]

Type: <b><a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">FAX_SERVER_EVENTS_TYPE_ENUM</a></b>

A value that contains a set of bit flags representing the types of events for which the <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object is registering to receive notifications. For more information, see <a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">FAX_SERVER_EVENTS_TYPE_ENUM</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In Microsoft Visual Basic, if you want the fax server to receive notifications, you have to create the <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object using the following syntax:


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
Dim WithEvents objFaxServer As New FAXCOMEXLib.FaxServer
Set objFaxServer = CreateObject("FaxServer") 
</pre>
</td>
</tr>
</table></span></div>
In Microsoft Visual C++, the <a href="https://msdn.microsoft.com/e8192f70-b0aa-4055-b67b-ff95991b66f2">IFaxServerNotify</a> interface on the <b>FaxServer</b> object receives notifications of the events.


By default, the <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object does not receive notifications for any server events. If you want the <b>FaxServer</b> object to receive notifications, you must call <b>IFaxServer::ListenToServerEvents</b> and pass to it the event types for which you want to receive notifications. To stop receiving the notification, call this method with <i>EventTypes</i> equal to <a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">fsetNONE</a>.

Access rights for this method depend on which events are requested, as shown in the following table.


<table class="clsStd">
<tr>
<td>Event</td>
<td>Required access rights</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">fsetINCOMING_CALL</a>
</td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">fsetIN_QUEUE</a>
</td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_JOBS</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">fsetOUT_QUEUE</a>
</td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_JOBS</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">fsetCONFIG</a>
</td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">fsetDEVICE_STATUS</a>
</td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">fsetACTIVITY</a>
</td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">fsetIN_ARCHIVE</a>
</td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f1d4298b-4e9a-42c1-8e1d-7331d8714c47">fsetOUT_ARCHIVE</a>
</td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_OUT_ARCHIVE</a>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/a02d2bc4-bbee-4eb5-8e19-6032957155ce">Registering for Event Notifications</a>



<a href="https://msdn.microsoft.com/3a9f42fa-383a-4072-92a6-b59f7940ab04">Visual Basic Example</a>
 

 


---
UID: NF:faxcomex.IFaxServer.ListenToServerEvents
title: IFaxServer::ListenToServerEvents (faxcomex.h)
author: windows-sdk-content
description: The IFaxServer::ListenToServerEvents method registers the FaxServer object to receive notifications about one or more types of server events, or to stop these notifications.
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_listentoserverevents_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8kmr.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],ListenToServerEvents method, IFaxServer.ListenToServerEvents, IFaxServer::ListenToServerEvents, ListenToServerEvents, ListenToServerEvents method [Fax Service], ListenToServerEvents method [Fax Service],IFaxServer interface, _mfax_faxserver.listentoserverevents, fax._mfax_faxserver_cpp_mfax_faxserver_listentoserverevents_cpp, fax._mfax_faxserver_listentoserverevents, faxcomex/IFaxServer::ListenToServerEvents
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
ms.custom: 19H1
---

# IFaxServer::ListenToServerEvents


## -description


The <b>IFaxServer::ListenToServerEvents</b> method registers the <a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a> object to receive notifications about one or more types of server events, or to stop these notifications. 


## -parameters




### -param EventTypes [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">FAX_SERVER_EVENTS_TYPE_ENUM</a></b>

A value that contains a set of bit flags representing the types of events for which the <a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a> object is registering to receive notifications. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">FAX_SERVER_EVENTS_TYPE_ENUM</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In Microsoft Visual Basic, if you want the fax server to receive notifications, you have to create the <a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a> object using the following syntax:



```

Dim WithEvents objFaxServer As New FAXCOMEXLib.FaxServer
Set objFaxServer = CreateObject("FaxServer") 

```


In Microsoft Visual C++, the <a href="https://msdn.microsoft.com/e8192f70-b0aa-4055-b67b-ff95991b66f2">IFaxServerNotify</a> interface on the <b>FaxServer</b> object receives notifications of the events.


By default, the <a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a> object does not receive notifications for any server events. If you want the <b>FaxServer</b> object to receive notifications, you must call <b>IFaxServer::ListenToServerEvents</b> and pass to it the event types for which you want to receive notifications. To stop receiving the notification, call this method with <i>EventTypes</i> equal to <a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">fsetNONE</a>.

Access rights for this method depend on which events are requested, as shown in the following table.


<table class="clsStd">
<tr>
<td>Event</td>
<td>Required access rights</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">fsetINCOMING_CALL</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_IN_ARCHIVE</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">fsetIN_QUEUE</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">fsetOUT_QUEUE</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">fsetCONFIG</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">fsetDEVICE_STATUS</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">fsetACTIVITY</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">fsetIN_ARCHIVE</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_IN_ARCHIVE</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689206(v=VS.85).aspx">fsetOUT_ARCHIVE</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_OUT_ARCHIVE</a>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689110(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693008(v=VS.85).aspx">Registering for Event Notifications</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693013(v=VS.85).aspx">Visual Basic Example</a>
 

 


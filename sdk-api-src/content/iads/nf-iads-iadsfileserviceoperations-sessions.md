---
UID: NF:iads.IADsFileServiceOperations.Sessions
title: IADsFileServiceOperations::Sessions
author: windows-sdk-content
description: The IADsFileServiceOperations::Sessions method gets a pointer to a pointer to the IADsCollection interface on a collection of the session objects that represent the current open sessions for this file service.
old-location: adsi\iadsfileserviceoperations_sessions.htm
tech.root: ADSI
ms.assetid: 97b485c9-650a-4d87-adbb-51799581c3bc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsFileServiceOperations interface [ADSI],Sessions method, IADsFileServiceOperations.Sessions, IADsFileServiceOperations::Sessions, Sessions, Sessions method [ADSI], Sessions method [ADSI],IADsFileServiceOperations interface, _ds_iadsfileserviceoperations_sessions, adsi.iadsfileserviceoperations__sessions, adsi.iadsfileserviceoperations_sessions, iads/IADsFileServiceOperations::Sessions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsFileServiceOperations.Sessions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsFileServiceOperations::Sessions


## -description


The <b>IADsFileServiceOperations::Sessions</b> method gets a pointer to a pointer to the  <a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a> interface on a collection of the session objects that represent the current open sessions for this file service.


## -parameters




### -param ppSessions [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a> interface used to enumerate objects that implement the  <a href="https://msdn.microsoft.com/54621f0d-7478-4a6f-a96f-f3f93e64b281">IADsSession</a> interface and represent the current open sessions for this file service.


## -returns



This method supports the standard return values including S_OK. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



Traditional directory services supply data only about directory service elements represented in the underlying data store. Data about sessions for file services may not be available from the underlying store.


#### Examples

The following code example shows how to enumerate active sessions managed by a file service.


```vb
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operation on "myComputer" 
' in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
For Each session In fso.sessions
    MsgBox "Session name: " & session.Name
Next session

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing

```


For a code example using the <b>IADsFileServiceOperations::Sessions</b> interface, see the code example given in  <a href="https://msdn.microsoft.com/54621f0d-7478-4a6f-a96f-f3f93e64b281">IADsSession</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="https://msdn.microsoft.com/328eedfe-7fdc-4e90-8bac-ab30944b8fbf">IADsFileService</a>



<a href="https://msdn.microsoft.com/91335658-8efb-4945-9862-f72e78d749d6">IADsFileServiceOperations</a>



<a href="https://msdn.microsoft.com/54621f0d-7478-4a6f-a96f-f3f93e64b281">IADsSession</a>
 

 


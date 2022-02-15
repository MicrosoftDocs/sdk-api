---
UID: NN:iads.IADsSession
title: IADsSession (iads.h)
description: The IADsSession interface is a dual interface that inherits from IADs. It is designed to represent an active session for file service across a network.
helpviewer_keywords: ["IADsSession","IADsSession interface [ADSI]","IADsSession interface [ADSI]","described","_ds_iadssession","adsi.iadssession","iads/IADsSession"]
old-location: adsi\iadssession.htm
tech.root: adsi
ms.assetid: 54621f0d-7478-4a6f-a96f-f3f93e64b281
ms.date: 12/05/2018
ms.keywords: IADsSession, IADsSession interface [ADSI], IADsSession interface [ADSI],described, _ds_iadssession, adsi.iadssession, iads/IADsSession
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsSession
 - iads/IADsSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsSession
---

# IADsSession interface


## -description

The <b>IADsSession</b> interface is a dual interface that inherits from  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to represent an active session for file service across a network.

## -inheritance

The <b>IADsSession</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsSession</b> also has these types of members:

## -remarks

When a remote user opens resources on a target computer, an active session is established between the remote user and that computer. Many resources can be opened in a single active session. ADSI represents this process with a session object that implements this interface.

Call the methods of this interface to examine session-specific data, for example, who is using the session, which computer is used, and the time elapsed for the current session.

Sessions are managed by the file service. To obtain session objects, first bind to this service ("LanmanServer" or "FPNW").


#### Examples

The following code example shows how to bind to a session.


```vb
Dim fso as IADsFileServiceOperations
Dim ss as IADsCollection

On Error GoTo Cleanup
 
Set fso = GetObject("WinNT://myComputer/LanmanServer")
Set ss = fso.Sessions

' Insert code to access session data.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
    Set ss = Nothing
```

---
UID: NN:iads.IADsService
title: IADsService (iads.h)
description: The IADsService interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsService","IADsService interface [ADSI]","IADsService interface [ADSI]","described","_ds_iadsservice","adsi.iadsservice","iads/IADsService"]
old-location: adsi\iadsservice.htm
tech.root: adsi
ms.assetid: b59a6594-1109-4913-8a83-4888e56e71d0
ms.date: 12/05/2018
ms.keywords: IADsService, IADsService interface [ADSI], IADsService interface [ADSI],described, _ds_iadsservice, adsi.iadsservice, iads/IADsService
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
 - IADsService
 - iads/IADsService
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
 - IADsService
---

# IADsService interface


## -description

The <b>IADsService</b> interface is a dual interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to maintain data about system services running on a host computer. Examples of such services include "FAX" for Microsoft Fax Service, "RemoteAccess" for Routing and RemoteAccess Service, and "seclogon" for Secondary Logon Service. Examples of the data about any system service include the path to the executable file on the host computer, the type of the service, other services or load group required to run a particular service, and others. <b>IADsService</b> exposes several properties to represent such data.

## -inheritance

The <b>IADsService</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsService</b> also has these types of members:

## -remarks

The system services are published in the underlying directory. Some may be running, others may not. To verify the status or to operate on any of the services, use the properties and methods of the  <a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a> interface.

File service is a special case of the system service. The  <a href="/windows/desktop/api/iads/nn-iads-iadsfileservice">IADsFileService</a> and  <a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a> interfaces support additional features unique to file services.


#### Examples

To identify services available on a host computer, first bind to the computer and then enumerate the services available on that computer. The following code example shows  how to do this.


```vb
Public Sub ListServicesOnComputer(ComputerName As String)
    Dim comp As IADsComputer
    Dim srvc As IADsServiceOperations
    
    On Error GoTo Cleanup
    
    Set comp = GetObject("WinNT://" + ComputerName + ",Computer")
    comp.Filter = Array("Service")
    For Each srvc In comp
        ' The srvc object is an IADsServiceOperations object that can be 
        ' used to obtain the status of the service with the Status property. 
        ' Other IADs properties can also be obtained.
    Next
    
Cleanup:
    If (Err.Number <> 0) Then
        MsgBox (Err.Description & vbLf & vbLf & " Error number = " & Err.Number)
    End If
    Set comp = Nothing
End Sub
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsfileservice">IADsFileService</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>



<a href="/windows/desktop/ADSI/iadsservice-property-methods">IADsService Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

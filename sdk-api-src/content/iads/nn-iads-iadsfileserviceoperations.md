---
UID: NN:iads.IADsFileServiceOperations
title: IADsFileServiceOperations (iads.h)
description: The IADsFileServiceOperations interface is a dual interface that inherits from IADsServiceOperations.
helpviewer_keywords: ["IADsFileServiceOperations","IADsFileServiceOperations interface [ADSI]","IADsFileServiceOperations interface [ADSI]","described","_ds_iadsfileserviceoperations","adsi.iadsfileserviceoperations","iads/IADsFileServiceOperations"]
old-location: adsi\iadsfileserviceoperations.htm
tech.root: adsi
ms.assetid: 91335658-8efb-4945-9862-f72e78d749d6
ms.date: 12/05/2018
ms.keywords: IADsFileServiceOperations, IADsFileServiceOperations interface [ADSI], IADsFileServiceOperations interface [ADSI],described, _ds_iadsfileserviceoperations, adsi.iadsfileserviceoperations, iads/IADsFileServiceOperations
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
 - IADsFileServiceOperations
 - iads/IADsFileServiceOperations
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
 - IADsFileServiceOperations
---

# IADsFileServiceOperations interface


## -description

The <b>IADsFileServiceOperations</b> interface is a dual interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>. It extends the functionality, as exposed in the  <b>IADsServiceOperations</b> interface, for managing the file service across a network. Specifically, it serves to maintain and manage open resources and active sessions of the file service.

## -inheritance

The <b>IADsFileServiceOperations</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>, <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>, and <a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>. <b>IADsFileServiceOperations</b> also has these types of members:

## -remarks

To bind to a file service operations object, use the ADsPath string that identifies the "LanmanServer" service on the host computer, as shown in the following code example.


```vb
Dim fso As IADsFileServiceOperations
On Error Resume Next

' Replace aDomain with the domain that the computer is located on.
' Replace aComputer with the name of the computer.
Set fso = GetObject("WinNT://aDomain/aComputer/LanmanServer")
```


From this point, you can handle the file service object as just a service object, applying any of the methods of <a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a> to the file service object. For example, you can examine the operational status of the file service, start or stop the file service, or change its password.

However, the <b>IADsFileServiceOperations</b> interface allows you to work with open resources and active sessions of the file service. See the following example.


```vb
For Each r in fso.Resources
MsgBox r.User
MsgBox r.Path
MsgBox r.LockCount
Next
```


For more information about active sessions and open resources, see  <a href="/windows/desktop/api/iads/nn-iads-iadssession">IADsSession</a> and  <a href="/windows/desktop/api/iads/nn-iads-iadsresource">IADsResource</a>.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsfileservice">IADsFileService</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsresource">IADsResource</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsservice">IADsService</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssession">IADsSession</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

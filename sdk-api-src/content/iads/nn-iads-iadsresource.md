---
UID: NN:iads.IADsResource
title: IADsResource (iads.h)
description: The IADsResource interface is a dual interface that inherits from IADs. It is designed to manage an open resource for a file service across a network.
helpviewer_keywords: ["IADsResource","IADsResource interface [ADSI]","IADsResource interface [ADSI]","described","_ds_iadsresource","adsi.iadsresource","iads/IADsResource"]
old-location: adsi\iadsresource.htm
tech.root: adsi
ms.assetid: 217749a4-55dc-457f-8582-1513ff3b0666
ms.date: 12/05/2018
ms.keywords: IADsResource, IADsResource interface [ADSI], IADsResource interface [ADSI],described, _ds_iadsresource, adsi.iadsresource, iads/IADsResource
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
 - IADsResource
 - iads/IADsResource
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
 - IADsResource
---

# IADsResource interface


## -description

The <b>IADsResource</b> interface is a dual interface that inherits from  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to manage an open resource for a file service across a network.

## -inheritance

The <b>IADsResource</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsResource</b> also has these types of members:

## -remarks

When a remote user opens a folder or a subfolder on a public share point on the target computer, ADSI considers this folder to be an open resource and represents it with a resource object that implements this interface.


#### Examples

The following code example shows how to obtain the collection of resource objects from a file service operations object.


```vb
Dim fso as IADsFileServiceOperations
Dim rs as IADsCollection
On Error GoTo Cleanup

Set fso = GetObject("WinNT://myHost/LanmanServer")
Set rs = fso.Resources

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set rso = Nothing
    Set rs = Nothing

```

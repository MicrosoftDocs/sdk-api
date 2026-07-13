---
UID: NN:iads.IADsFileShare
title: IADsFileShare (iads.h)
description: The IADsFileShare interface is a dual interface that inherits from IADs. It is designed for representing a published file share across the network. Call the methods on IADsFileShare to access or publish data about a file share point.
helpviewer_keywords: ["IADsFileShare","IADsFileShare interface [ADSI]","IADsFileShare interface [ADSI]","described","_ds_iadsfileshare","adsi.iadsfileshare","iads/IADsFileShare"]
old-location: adsi\iadsfileshare.htm
tech.root: adsi
ms.assetid: 37695195-fc33-499d-98c1-ccfd190cb2f9
ms.date: 12/05/2018
ms.keywords: IADsFileShare, IADsFileShare interface [ADSI], IADsFileShare interface [ADSI],described, _ds_iadsfileshare, adsi.iadsfileshare, iads/IADsFileShare
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
 - IADsFileShare
 - iads/IADsFileShare
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
 - IADsFileShare
---

# IADsFileShare interface


## -description

The <b>IADsFileShare</b> interface is a dual interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed for representing a published file share across the network. Call the methods on <b>IADsFileShare</b> to access or publish data about a file share point.

## -inheritance

The <b>IADsFileShare</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsFileShare</b> also has these types of members:

## -remarks

<b>IADsFileShare</b> is supported by WinNT system provider only. Using the WinNT provider, you can also bind to a FPNW share by substituting "FPNW" for "LanmanServer" in the code examples below.

To bind to a file share, using the WinNT system provider, you can explicitly bind to the file service "LanmanServer" on the host machine, and then enumerate the container to reach the file share of interest, or bind directly to the file share.


#### Examples

The following code example demonstrates how to bind to the file service and enumerate the container to display the names of the shares in that container.


```vb
Dim fs as IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://aComputer/LanmanServer")

For Each share In fs
    MsgBox("Share: " & share.name)
Next share

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing

```


The following code example demonstrates how to bind directly to a file share.


```vb
Dim fs as IADsFileShare
On Error Resume Next
Set fs = GetObject("WinNT://aComputer/LanmanServer/_file_share_name_")
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/ADSI/iadsfileshare-property-methods">IADsFileShare Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

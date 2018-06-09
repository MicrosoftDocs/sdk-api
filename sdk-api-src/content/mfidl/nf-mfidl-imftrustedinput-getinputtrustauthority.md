---
UID: NF:mfidl.IMFTrustedInput.GetInputTrustAuthority
title: IMFTrustedInput::GetInputTrustAuthority
author: windows-sdk-content
description: Retrieves the input trust authority (ITA) for a specified stream.
old-location: mf\imftrustedinput_getinputtrustauthority.htm
old-project: medfound
ms.assetid: b4ebf02e-554a-4e7e-93d3-6f37d8b689bf
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetInputTrustAuthority, GetInputTrustAuthority method [Media Foundation], GetInputTrustAuthority method [Media Foundation],IMFTrustedInput interface, IMFTrustedInput interface [Media Foundation],GetInputTrustAuthority method, IMFTrustedInput.GetInputTrustAuthority, IMFTrustedInput::GetInputTrustAuthority, b4ebf02e-554a-4e7e-93d3-6f37d8b689bf, mf.imftrustedinput_getinputtrustauthority, mfidl/IMFTrustedInput::GetInputTrustAuthority
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTrustedInput.GetInputTrustAuthority
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTrustedInput::GetInputTrustAuthority


## -description



Retrieves the input trust authority (ITA) for a specified stream.




## -parameters




### -param dwStreamID [in]

The stream identifier for which the ITA is being requested.


### -param riid [in]

The interface identifier (IID) of the interface being requested. Currently the only supported value is IID_IMFInputTrustAuthority.


### -param ppunkObject [out]

Receives a pointer to the ITA's <b>IUnknown</b> interface. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The ITA does not expose the requested interface.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/637e0225-6fd8-4b83-b4fb-119e7a5ef5d2">IMFInputTrustAuthority</a>



<a href="https://msdn.microsoft.com/59a9def7-69a6-4f80-bb5e-1cb372ff6eab">IMFTrustedInput</a>
 

 


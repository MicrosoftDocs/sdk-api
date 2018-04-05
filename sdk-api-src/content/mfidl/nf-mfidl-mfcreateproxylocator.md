---
UID: NF:mfidl.MFCreateProxyLocator
title: MFCreateProxyLocator function
author: windows-driver-content
description: Creates a default proxy locator.
old-location: mf\mfcreateproxylocator.htm
old-project: medfound
ms.assetid: 9ad707df-533a-407b-a611-49bfb019affc
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 9ad707df-533a-407b-a611-49bfb019affc, MFCreateProxyLocator, MFCreateProxyLocator function [Media Foundation], mf.mfcreateproxylocator, mfidl/MFCreateProxyLocator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateProxyLocator
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateProxyLocator function


## -description



Creates a default proxy locator.




## -parameters




### -param pszProtocol [in]

The name of the protocol.

<div class="alert"><b>Note</b>  In this release of Media Foundation, the default proxy locator does not support RTSP.</div>
<div> </div>

### -param pProxyConfig [in]

Pointer to the <b>IPropertyStore</b> interface of a property store that contains the proxy configuration in the <a href="https://msdn.microsoft.com/85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3">MFNETSOURCE_PROXYSETTINGS</a> property.


### -param ppProxyLocator [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/2906b998-f1ca-4c65-b810-cbc360390653">IMFNetProxyLocator</a> interface. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

                The function succeeded.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/e739746d-2a09-4237-a7c1-0aed4e4516d7">Proxy Support for Network Sources</a>
 

 


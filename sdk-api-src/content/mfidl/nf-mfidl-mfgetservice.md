---
UID: NF:mfidl.MFGetService
title: MFGetService function
author: windows-driver-content
description: Queries an object for a specified service interface.
old-location: mf\mfgetservice.htm
old-project: medfound
ms.assetid: 119e9e2f-0e26-4dfc-9c89-156b63a63640
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: 119e9e2f-0e26-4dfc-9c89-156b63a63640, MFGetService, MFGetService function [Media Foundation], mf.mfgetservice, mfidl/MFGetService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFGetService
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFGetService function


## -description


Queries an object for a specified service interface.

This function is a helper function that wraps the <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> method. The function queries the object for the <a href="https://msdn.microsoft.com/102a1dff-8419-4f86-a145-53ce3d0123f5">IMFGetService</a> interface and, if successful, calls <b>GetService</b> on the object.


## -parameters




### -param punkObject

A pointer to the <b>IUnknown</b> interface of the object to query.
          


### -param guidService

The service identifier (SID) of the service. For a list of service identifiers, see <a href="https://msdn.microsoft.com/264a0e86-49e9-4777-956b-a83e9db52a25">Service Interfaces</a>.
          


### -param riid

The interface identifier (IID) of the interface being requested.
          


### -param ppvObject

Receives the interface pointer. The caller must release the interface.
          


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

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_SERVICE</b></dt>
</dl>
</td>
<td width="60%">

                The service requested cannot be found in the object represented by <i>punkObject</i>.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/102a1dff-8419-4f86-a145-53ce3d0123f5">IMFGetService</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/264a0e86-49e9-4777-956b-a83e9db52a25">Service Interfaces</a>
 

 


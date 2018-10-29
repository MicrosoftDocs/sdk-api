---
UID: NF:mfapi.MFEndCreateFile
title: MFEndCreateFile function
author: windows-sdk-content
description: Completes an asynchronous request to create a byte stream from a file.
old-location: mf\mfendcreatefile.htm
tech.root: medfound
ms.assetid: daa92660-5d0d-4c7c-985a-ad621eca4bfc
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: MFEndCreateFile, MFEndCreateFile function [Media Foundation], daa92660-5d0d-4c7c-985a-ad621eca4bfc, mf.mfendcreatefile, mfapi/MFEndCreateFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFEndCreateFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFEndCreateFile function


## -description



Completes an asynchronous request to create a byte stream from a file.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">Invoke</a> method.


### -param ppFile [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of the byte stream. The caller must release the interface.


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
 




## -remarks



Call this function when the <a href="https://msdn.microsoft.com/aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd">MFBeginCreateFile</a> function completes asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd">MFBeginCreateFile</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 


---
UID: NF:mfidl.MFCreatePMPServer
title: MFCreatePMPServer function
author: windows-driver-content
description: Creates the protected media path (PMP) server object.
old-location: mf\mfcreatepmpserver.htm
old-project: medfound
ms.assetid: 2bf5541e-9b7e-4e7a-a868-4956c1f70882
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 2bf5541e-9b7e-4e7a-a868-4956c1f70882, MFCreatePMPServer, MFCreatePMPServer function [Media Foundation], mf.mfcreatepmpserver, mfidl/MFCreatePMPServer
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
-	MFCreatePMPServer
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreatePMPServer function


## -description



Creates the protected media path (PMP) server object.




## -parameters




### -param dwCreationFlags [in]

A member of the <a href="https://msdn.microsoft.com/6341aaff-aa80-4172-8577-0b757a01ea53">MFPMPSESSION_CREATION_FLAGS</a> enumeration that specifies how to create the PMP session.


### -param ppPMPServer [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/ba6dc70a-d77d-41de-afe1-65f2efcc4a95">IMFPMPServer</a> interface. The caller must release the interface.


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
 

 


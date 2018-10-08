---
UID: NF:mfidl.MFCreateNetSchemePlugin
title: MFCreateNetSchemePlugin function
author: windows-sdk-content
description: Creates the scheme handler for the network source.
old-location: mf\mfcreatenetschemeplugin.htm
tech.root: medfound
ms.assetid: f08de332-2b05-4fee-be45-d4928f5f4ef2
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: MFCreateNetSchemePlugin, MFCreateNetSchemePlugin function [Media Foundation], f08de332-2b05-4fee-be45-d4928f5f4ef2, mf.mfcreatenetschemeplugin, mfidl/MFCreateNetSchemePlugin
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateNetSchemePlugin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateNetSchemePlugin function


## -description



Creates the scheme handler for the network source.




## -parameters




### -param riid [in]

Interface identifier (IID) of the interface to retrieve.


### -param ppvHandler [out]

Receives a pointer to the requested interface. The caller must release the interface. The scheme handler exposes the <a href="https://msdn.microsoft.com/a342054e-2cb5-494a-a2f7-d144c72d1fa5">IMFSchemeHandler</a> interface.


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
 

 


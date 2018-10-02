---
UID: NF:wmcontainer.MFCreatePresentationDescriptorFromASFProfile
title: MFCreatePresentationDescriptorFromASFProfile function
author: windows-sdk-content
description: Creates a presentation descriptor from an ASF profile object.
old-location: mf\mfcreatepresentationdescriptorfromasfprofile.htm
tech.root: MedFound
ms.assetid: e36ac685-4ebe-4fc6-a17a-f36b9d667add
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MFCreatePresentationDescriptorFromASFProfile, MFCreatePresentationDescriptorFromASFProfile function [Media Foundation], e36ac685-4ebe-4fc6-a17a-f36b9d667add, mf.mfcreatepresentationdescriptorfromasfprofile, wmcontainer/MFCreatePresentationDescriptorFromASFProfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wmcontainer.h
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
 - MFCreatePresentationDescriptorFromASFProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreatePresentationDescriptorFromASFProfile function


## -description



Creates a presentation descriptor from an ASF profile object.




## -parameters




### -param pIProfile

Pointer to the <a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a> interface of the ASF profile object.


### -param ppIPD

Receives a pointer to the <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface. The caller must release the interface.


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
 

 


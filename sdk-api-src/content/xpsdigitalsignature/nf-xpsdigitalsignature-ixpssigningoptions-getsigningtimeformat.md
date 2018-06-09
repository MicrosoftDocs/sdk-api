---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetSigningTimeFormat
title: IXpsSigningOptions::GetSigningTimeFormat
author: windows-sdk-content
description: Gets the format of the signing time string.
old-location: xps\ixpssigningoptions_getsigningtimeformat.htm
old-project: printdocs
ms.assetid: 79af4463-1651-44d2-9143-b1f922ba5cfb
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetSigningTimeFormat, GetSigningTimeFormat method [XPS Documents and Packaging], GetSigningTimeFormat method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetSigningTimeFormat method, IXpsSigningOptions.GetSigningTimeFormat, IXpsSigningOptions::GetSigningTimeFormat, xps.ixpssigningoptions_getsigningtimeformat, xpsdigitalsignature/IXpsSigningOptions::GetSigningTimeFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_SIGN_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSigningOptions.GetSigningTimeFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSigningOptions::GetSigningTimeFormat


## -description


Gets the format of the signing time string.


## -parameters




### -param timeFormat [out, retval]

The <a href="https://msdn.microsoft.com/9b8ff585-5795-48ce-b2fd-a49e3d34ccb9">OPC_SIGNATURE_TIME_FORMAT</a> value that specifies the format of the signing time string.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the format of the date-time string that is passed in <i>timeFormat</i>, see <a href="https://msdn.microsoft.com/9b8ff585-5795-48ce-b2fd-a49e3d34ccb9">OPC_SIGNATURE_TIME_FORMAT</a>.

If a signing time format has not been set,  <b>OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS</b> will be used as the default format.




## -see-also




<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="https://msdn.microsoft.com/9b8ff585-5795-48ce-b2fd-a49e3d34ccb9">OPC_SIGNATURE_TIME_FORMAT</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


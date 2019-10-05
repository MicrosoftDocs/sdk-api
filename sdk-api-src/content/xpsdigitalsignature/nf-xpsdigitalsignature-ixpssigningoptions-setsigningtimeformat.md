---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetSigningTimeFormat
title: IXpsSigningOptions::SetSigningTimeFormat (xpsdigitalsignature.h)
author: windows-sdk-content
description: Sets the format of the signing time string.
old-location: xps\ixpssigningoptions_setsigningtimeformat.htm
tech.root: printdocs
ms.assetid: 55ed2bb7-56d0-41d6-a8c3-dc0ff8cde7f8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetSigningTimeFormat method, IXpsSigningOptions.SetSigningTimeFormat, IXpsSigningOptions::SetSigningTimeFormat, SetSigningTimeFormat, SetSigningTimeFormat method [XPS Documents and Packaging], SetSigningTimeFormat method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setsigningtimeformat, xpsdigitalsignature/IXpsSigningOptions::SetSigningTimeFormat
ms.topic: method
f1_keywords: 
 - "xpsdigitalsignature/IXpsSigningOptions.SetSigningTimeFormat"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSigningOptions.SetSigningTimeFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSigningOptions::SetSigningTimeFormat


## -description


Sets the format of the signing time string.


## -parameters




### -param timeFormat [in]

The <a href="https://docs.microsoft.com/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a> value that specifies the format of the signing time string.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the format of the date-time string that is  passed in <i>timeFormat</i>, see <a href="https://docs.microsoft.com/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a>.

If a signing time format has not been set,   <b>OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS</b>  will be used as the default format.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://docs.microsoft.com/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


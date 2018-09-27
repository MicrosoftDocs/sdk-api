---
UID: NE:dshowasf._AM_ASFWRITERCONFIG_PARAM
title: "_AM_ASFWRITERCONFIG_PARAM"
author: windows-sdk-content
description: The _AM_ASFWRITERCONFIG_PARAM DirectShow QASF enumeration type defines filter configuration parameters used in the IConfigAsfWriter2::GetParam and SetParam methods.
old-location: wmformat\_am_asfwriterconfig_param_enumeration.htm
tech.root: wmformat
ms.assetid: 773f9b98-8b88-4b2d-b1f0-40bb1e0c0ab0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: AM_CONFIGASFWRITER_PARAM_AUTOINDEX, AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS, AM_CONFIGASFWRITER_PARAM_MULTIPASS, _AM_ASFWRITERCONFIG_PARAM, _AM_ASFWRITERCONFIG_PARAM enumeration [windows Media Format], dshowasf/AM_CONFIGASFWRITER_PARAM_AUTOINDEX, dshowasf/AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS, dshowasf/AM_CONFIGASFWRITER_PARAM_MULTIPASS, dshowasf/_AM_ASFWRITERCONFIG_PARAM, wmformat._am_asfwriterconfig_param_enumeration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dshowasf.h
api_name:
 - _AM_ASFWRITERCONFIG_PARAM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _AM_ASFWRITERCONFIG_PARAM enumeration


## -description



The <b>_AM_ASFWRITERCONFIG_PARAM</b> DirectShow QASF enumeration type defines filter configuration parameters used in the <a href="https://msdn.microsoft.com/81d915a1-6190-46e3-a5cb-7f5fc242b8dd">IConfigAsfWriter2::GetParam</a> and <a href="https://msdn.microsoft.com/b8067fb2-c379-4b26-b4f7-c790604e3edc">SetParam</a> methods.




## -enum-fields




### -field AM_CONFIGASFWRITER_PARAM_AUTOINDEX

Indicates whether the <a href="https://msdn.microsoft.com/a902c92e-836d-492c-b2d2-89c216125774">WM ASF Writer</a> should automatically create a temporal index after it has completed encoding a file. Set this parameter to <b>FALSE</b> if you want to create a frame-based index using the Windows Media Format SDK directly.


### -field AM_CONFIGASFWRITER_PARAM_MULTIPASS

Indicates whether the filter should operate in two-pass mode. See Remarks.


### -field AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS

Indicates that the <a href="https://msdn.microsoft.com/a902c92e-836d-492c-b2d2-89c216125774">WM ASF Writer</a> will not attempt to compress the input streams. Use this flag to pack content that is not Windows Media–based into an ASF file.


## -remarks



In two-pass mode the filter makes two passes through the file. In the first pass, the filter examines each media stream in its entirety to determine the optimal encoding parameters for the file. The actual encoding is performed in the second pass. Therefore, to create an ASF file in two-pass mode, you must run the graph, wait for an <b>EC_PREPROCESS_COMPLETE</b> event, seek to the beginning of the source file, and then run the graph a second time.

<div class="alert"><b>Important</b>  To receive the <b>EC_PREPROCESS_COMPLETE</b> event you must use the DirectShow <b>GetEvent</b> method as demonstrated in the DSCopy sample. The DirectShow <b>WaitForCompletion</b> method will not receive this particular event.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a462fc8b-5a2e-4c93-828d-177d1965b734">Configuring Profiles and Other File Properties (QASF)</a>



<a href="https://msdn.microsoft.com/66f483b5-3886-48b4-bc43-7c3517abd20d">DirectShow QASF Reference</a>



<a href="https://msdn.microsoft.com/81d915a1-6190-46e3-a5cb-7f5fc242b8dd">IConfigAsfWriter2::GetParam</a>



<a href="https://msdn.microsoft.com/b8067fb2-c379-4b26-b4f7-c790604e3edc">IConfigAsfWriter2::SetParam</a>
 

 


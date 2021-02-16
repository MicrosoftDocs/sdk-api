---
UID: NF:wmcodecdsp.ITocParser.Init
title: ITocParser::Init (wmcodecdsp.h)
description: The Init method initializes the TOC Parser object and associates it with a media file.
helpviewer_keywords: ["ITocParser interface [Media Foundation]","Init method","ITocParser.Init","ITocParser::Init","Init","Init method [Media Foundation]","Init method [Media Foundation]","ITocParser interface","codecapi.itocparser_init","mf.itocparser_init","wmcodecdsp/ITocParser::Init"]
old-location: mf\itocparser_init.htm
tech.root: mf
ms.assetid: 8d7a9bda-56e8-4b42-ace5-4d6cf5d52b59
ms.date: 12/05/2018
ms.keywords: ITocParser interface [Media Foundation],Init method, ITocParser.Init, ITocParser::Init, Init, Init method [Media Foundation], Init method [Media Foundation],ITocParser interface, codecapi.itocparser_init, mf.itocparser_init, wmcodecdsp/ITocParser::Init
req.header: wmcodecdsp.h
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
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITocParser::Init
 - wmcodecdsp/ITocParser::Init
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocParser.Init
---

# ITocParser::Init


## -description

The <b>Init</b> method initializes the TOC Parser object and associates it with a media file.

## -parameters

### -param pwszFileName [in]

Pointer to a NULL-terminated wide-character string that specifies the path of the media file. See Remarks.

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
</table>

## -remarks

The path that you pass in <i>pwszFileName</i> must be a long Universal Naming Convention (UNC) file path. A long UNC file path begins with "\\?\". The following line of code shows how to set the path for the file c:\experiment\seattle.wmv.

<code>pTocParser-&gt;Init(L"\\\\?\\c:\\experiment\\seattle.wmv");</code>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser">ITocParser</a>
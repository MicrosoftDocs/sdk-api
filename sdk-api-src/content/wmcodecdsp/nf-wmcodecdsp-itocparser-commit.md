---
UID: NF:wmcodecdsp.ITocParser.Commit
title: ITocParser::Commit (wmcodecdsp.h)
description: The Commit method stores the current state of the TOC Parser object in its associated media file.
helpviewer_keywords: ["Commit","Commit method [Media Foundation]","Commit method [Media Foundation]","ITocParser interface","ITocParser interface [Media Foundation]","Commit method","ITocParser.Commit","ITocParser::Commit","codecapi.itocparser_commit","mf.itocparser_commit","wmcodecdsp/ITocParser::Commit"]
old-location: mf\itocparser_commit.htm
tech.root: mf
ms.assetid: 549c170e-2e4d-4edb-b84e-178bfbb13fed
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Media Foundation], Commit method [Media Foundation],ITocParser interface, ITocParser interface [Media Foundation],Commit method, ITocParser.Commit, ITocParser::Commit, codecapi.itocparser_commit, mf.itocparser_commit, wmcodecdsp/ITocParser::Commit
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
 - ITocParser::Commit
 - wmcodecdsp/ITocParser::Commit
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
 - ITocParser.Commit
---

# ITocParser::Commit


## -description

The <b>Commit</b> method stores the current state of the TOC Parser object in its associated media file.



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

You can associate a TOC Parser object with a media file by calling <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init">ITocParser::Init</a>. As you add, modify, or remove tables of contents from the TOC Parser object, those changes are made only to the TOC Parser object in memory, not to the media file. To store your changes in the media file, you must call <b>ITocParser::Commit</b>.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser">ITocParser</a>

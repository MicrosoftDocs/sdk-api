---
UID: NN:objidl.ISurrogate
title: ISurrogate (objidl.h)
description: Used to dynamically load new DLL servers into an existing surrogate and free the surrogate when it is no longer needed.
helpviewer_keywords: ["ISurrogate","ISurrogate interface [COM]","ISurrogate interface [COM]","described","_com_isurrogate","com.isurrogate","objidlbase/ISurrogate"]
old-location: com\isurrogate.htm
tech.root: com
ms.assetid: fbed0514-3646-4744-aa7a-4a98f1a12cc0
ms.date: 12/05/2018
ms.keywords: ISurrogate, ISurrogate interface [COM], ISurrogate interface [COM],described, _com_isurrogate, com.isurrogate, objidlbase/ISurrogate
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISurrogate
 - objidl/ISurrogate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISurrogate
---

# ISurrogate interface


## -description

Used to dynamically load new DLL servers into an existing surrogate and free the surrogate when it is no longer needed.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISurrogate</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISurrogate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISurrogate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/objidl/nf-objidl-isurrogate-freesurrogate">FreeSurrogate</a>
</td>
<td align="left" width="63%">
Unloads a DLL server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/objidl/nf-objidl-isurrogate-loaddllserver">LoadDllServer</a>
</td>
<td align="left" width="63%">
Loads a DLL server into the implementing surrogate.

</td>
</tr>
</table>

## -remarks

A surrogate is an EXE process into which a DLL server can be loaded to give the DLL server the advantages of an EXE server without the coding overhead. It can also allow independent DLL servers to be located together within a single process, reducing the total number of processes needed. DLL servers are easy to write using standard development tools, like Microsoft Visual Studio, and running them in a surrogate process provides the benefits of an executable implementation, including fault isolation, the ability to serve multiple clients simultaneously, and allowing the server to provide services to remote clients in a distributed environment.

## -see-also

<a href="/windows/desktop/com/dll-surrogates">DLL Surrogates</a>



<a href="/windows/desktop/com/writing-a-custom-surrogate">Writing a Custom Surrogate</a>
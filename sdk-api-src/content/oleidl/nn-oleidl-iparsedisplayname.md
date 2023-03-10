---
UID: NN:oleidl.IParseDisplayName
title: IParseDisplayName (oleidl.h)
description: Parses a displayable name string to convert it into a moniker for custom moniker implementations.
helpviewer_keywords: ["IParseDisplayName","IParseDisplayName interface [COM]","IParseDisplayName interface [COM]","described","_com_iparsedisplayname","com.iparsedisplayname","oleidl/IParseDisplayName"]
old-location: com\iparsedisplayname.htm
tech.root: com
ms.assetid: 37844d9b-35ce-4d30-8a58-dac4c671896f
ms.date: 12/05/2018
ms.keywords: IParseDisplayName, IParseDisplayName interface [COM], IParseDisplayName interface [COM],described, _com_iparsedisplayname, com.iparsedisplayname, oleidl/IParseDisplayName
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.idl
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
 - IParseDisplayName
 - oleidl/IParseDisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IParseDisplayName
---

# IParseDisplayName interface


## -description

Parses a displayable name string to convert it into a moniker for custom moniker implementations.

Display name parsing is necessary when the end user inputs a string to identify a component, as in the following situations: 

<ul>
<li>A compound document application that supports linked components typically supports the <b>Edit:Links...</b> dialog box. Through this dialog box, the end user can enter a display name to specify a new link source for a specified linked component. The compound document needs to have this input string converted into a moniker.</li>
<li>A script language such as the macro language of a spreadsheet can allow textual references to a component. The language's interpreter needs to have such a reference converted into a moniker in order to execute the macro.</li>
</ul>This interface is not supported for use across machine boundaries.

## -inheritance

The <b>IParseDisplayName</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IParseDisplayName</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-parsedisplayname">IMoniker::ParseDisplayName</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a>



<a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a>



<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)">MkParseDisplayNameEx</a>

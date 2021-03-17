---
UID: NF:textserv.ShutdownTextServices
title: ShutdownTextServices function (textserv.h)
description: Disconnects a host from a text services instance.
helpviewer_keywords: ["ShutdownTextServices","ShutdownTextServices function [Windows Controls]","controls.shutdowntextservices","textserv/ShutdownTextServices"]
old-location: controls\shutdowntextservices.htm
tech.root: Controls
ms.assetid: 3367D22B-1F9E-4D70-8907-0F218A23AE7E
ms.date: 12/05/2018
ms.keywords: ShutdownTextServices, ShutdownTextServices function [Windows Controls], controls.shutdowntextservices, textserv/ShutdownTextServices
req.header: textserv.h
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ShutdownTextServices
 - textserv/ShutdownTextServices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msftedit.dll
api_name:
 - ShutdownTextServices
---

# ShutdownTextServices function


## -description

Disconnects a host from a text services instance.

## -parameters

### -param pTextServices [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A text services instance created by a previous call to the <a href="/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a> function.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the text services object was created successfully, the return value is S_OK. 

If the function fails, one of the following COM error codes are returned. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTextServices</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

A host calls this function when the host is being freed. Calling this function is necessary because all text services instances maintain a host pointer for which the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method has not been called. This function calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method on the text services instance and, if this is not the last reference to the text services object, nulls out the host pointer in the text services object and prepares the control to handle failed operations that require host services. This function allows any other outstanding references to the text services object to work or fail gracefully depending on the service required.

## -see-also

<a href="/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a>
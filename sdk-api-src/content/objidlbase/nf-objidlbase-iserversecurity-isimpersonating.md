---
UID: NF:objidlbase.IServerSecurity.IsImpersonating
title: IServerSecurity::IsImpersonating (objidlbase.h)
description: The IServerSecurity::IsImpersonating (objidlbase.h) method indicates whether the server is currently impersonating the client.
helpviewer_keywords: ["IServerSecurity interface [COM]","IsImpersonating method","IServerSecurity.IsImpersonating","IServerSecurity::IsImpersonating","IsImpersonating","IsImpersonating method [COM]","IsImpersonating method [COM]","IServerSecurity interface","_com_iserversecurity_isimpersonating","com.iserversecurity_isimpersonating","objidlbase/IServerSecurity::IsImpersonating"]
old-location: com\iserversecurity_isimpersonating.htm
tech.root: com
ms.assetid: f847348a-1785-4b4a-b43e-a5eea21847c4
ms.date: 08/15/2022
ms.keywords: IServerSecurity interface [COM],IsImpersonating method, IServerSecurity.IsImpersonating, IServerSecurity::IsImpersonating, IsImpersonating, IsImpersonating method [COM], IsImpersonating method [COM],IServerSecurity interface, _com_iserversecurity_isimpersonating, com.iserversecurity_isimpersonating, objidlbase/IServerSecurity::IsImpersonating
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IServerSecurity::IsImpersonating
 - objidlbase/IServerSecurity::IsImpersonating
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
 - IServerSecurity.IsImpersonating
---

# IServerSecurity::IsImpersonating


## -description

Indicates whether the server is currently impersonating the client.



## -returns

If the thread is currently impersonating, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a>

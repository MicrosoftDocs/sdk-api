---
UID: NF:shobjidl_core.IObjectWithProgID.GetProgID
title: IObjectWithProgID::GetProgID (shobjidl_core.h)

description: Retrieves the ProgID associated with an object.
old-location: shell\IObjectWithProgID_GetProgID.htm
tech.root: shell
ms.assetid: 37023615-09cb-4607-9496-7fe9d9f7c947

ms.date: 12/05/2018
ms.keywords: GetProgID, GetProgID method [Windows Shell], GetProgID method [Windows Shell],IObjectWithProgID interface, IObjectWithProgID interface [Windows Shell],GetProgID method, IObjectWithProgID.GetProgID, IObjectWithProgID::GetProgID, _shell_IObjectWithProgID_GetProgID, shell.IObjectWithProgID_GetProgID, shobjidl_core/IObjectWithProgID::GetProgID
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IObjectWithProgID.GetProgID"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IObjectWithProgID.GetProgID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectWithProgID::GetProgID


## -description


Retrieves the ProgID associated with an object.


## -parameters




### -param ppszProgID [out]

Type: <b>LPWSTR*</b>

A pointer to a string that, when this method returns successfully, contains the ProgID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithprogid">IObjectWithProgID</a>



<a href="https://docs.microsoft.com/windows/desktop/shell/fa-progids">Programmatic Identifiers</a>
 

 


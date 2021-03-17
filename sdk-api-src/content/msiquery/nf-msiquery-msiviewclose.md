---
UID: NF:msiquery.MsiViewClose
title: MsiViewClose function (msiquery.h)
description: The MsiViewClose function releases the result set for an executed view.
helpviewer_keywords: ["MsiViewClose","MsiViewClose function","_msi_msiviewclose","msiquery/MsiViewClose","setup.msiviewclose"]
old-location: setup\msiviewclose.htm
tech.root: setup
ms.assetid: bd38be52-d76c-4f1b-bc29-12f93aac2aa9
ms.date: 12/05/2018
ms.keywords: MsiViewClose, MsiViewClose function, _msi_msiviewclose, msiquery/MsiViewClose, setup.msiviewclose
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiViewClose
 - msiquery/MsiViewClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiViewClose
---

# MsiViewClose function


## -description

The 
<b>MsiViewClose</b> function releases the result set for an executed view.

## -parameters

### -param hView [in]

Handle to a view that is set to release.

## -returns

Note that in low memory situations, this function can raise a STATUS_NO_MEMORY exception.

## -remarks

The 
<b>MsiViewClose</b> function must be called before the 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewexecute">MsiViewExecute</a> function is called again on the view, unless all rows of the result set have been obtained with the 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewfetch">MsiViewFetch</a> function.

## -see-also

<a href="/windows/desktop/Msi/database-functions">General Database Access Functions</a>
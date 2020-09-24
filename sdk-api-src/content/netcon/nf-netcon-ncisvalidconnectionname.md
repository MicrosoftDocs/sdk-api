---
UID: NF:netcon.NcIsValidConnectionName
title: NcIsValidConnectionName function (netcon.h)
description: The NcIsValidConnectionName function verifies if the passed in connection name is valid.
helpviewer_keywords: ["NcIsValidConnectionName","NcIsValidConnectionName function [ICS/ICF]","ics.ncisvalidconnectionname","netcon/NcIsValidConnectionName"]
old-location: ics\ncisvalidconnectionname.htm
tech.root: ics
ms.assetid: 08fe9ba2-3314-45ff-8aea-742dd5b15560
ms.date: 12/05/2018
ms.keywords: NcIsValidConnectionName, NcIsValidConnectionName function [ICS/ICF], ics.ncisvalidconnectionname, netcon/NcIsValidConnectionName
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Netshell.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NcIsValidConnectionName
 - netcon/NcIsValidConnectionName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netshell.dll
api_name:
 - NcIsValidConnectionName
---

# NcIsValidConnectionName function


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>NcIsValidConnectionName</b> function verifies if the passed in connection name is valid.

## -parameters

### -param pszwName [in]

Connection name to check.

## -returns

<b>TRUE</b> if connection name is valid.

## -see-also

<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
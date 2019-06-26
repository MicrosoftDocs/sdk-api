---
UID: NF:dsclient.DsGetFriendlyClassName
title: DsGetFriendlyClassName function (dsclient.h)
author: windows-sdk-content
description: Retrieves the localized name for an object class.
old-location: ad\dsgetfriendlyclassname.htm
tech.root: ad
ms.assetid: 944b7227-2f22-418e-a9da-6fddec66876b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DsGetFriendlyClassName, DsGetFriendlyClassName function [Active Directory], ad.dsgetfriendlyclassname, dsclient/DsGetFriendlyClassName
ms.topic: function
f1_keywords: 
 - "dsclient/DsGetFriendlyClassName"
req.header: dsclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dsuiext.lib
req.dll: Dsuiext.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dsuiext.dll
api_name:
 - DsGetFriendlyClassName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsGetFriendlyClassName function


## -description


The <b>DsGetFriendlyClassName</b> function retrieves the localized name for an object class. This function is obsolete. New applications should use the <a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-getfriendlyclassname">IDsDisplaySpecifier::GetFriendlyClassName</a> method to perform this function.


## -parameters




### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to obtain the name of. Examples of the object class name are "user" and "container".


### -param pszBuffer [in]

Pointer to a wide character buffer that receives the name string. This buffer must be at least <i>cchBuffer</i> wide characters in length.


### -param cchBuffer [in]

Contains the size of the <i>pszBuffer</i> buffer, in wide characters, including the terminating <b>NULL</b> character. If the name exceeds this number of characters, the name is truncated.


## -returns



Returns a standard  <b>HRESULT</b> value, including the following.




## -remarks



If no friendly name is set in the display specifiers for the object class, this function returns the name passed in <i>pszObjectClass</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-getfriendlyclassname">IDsDisplaySpecifier::GetFriendlyClassName</a>
 

 


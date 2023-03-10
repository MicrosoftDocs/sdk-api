---
UID: NS:dsclient.DSPROPERTYPAGEINFO
title: DSPROPERTYPAGEINFO (dsclient.h)
description: The DSPROPERTYPAGEINFO structure is used by an Active Directory property sheet extension to obtain static registration data for the extension. This structure is supplied by the CFSTR_DSPROPERTYPAGEINFO clipboard format.
helpviewer_keywords: ["*LPDSPROPERTYPAGEINFO","DSPROPERTYPAGEINFO","DSPROPERTYPAGEINFO structure [Active Directory]","LPDSPROPERTYPAGEINFO","LPDSPROPERTYPAGEINFO structure pointer [Active Directory]","_glines_dspropertypageinfo","ad.dspropertypageinfo","dsclient/DSPROPERTYPAGEINFO","dsclient/LPDSPROPERTYPAGEINFO"]
old-location: ad\dspropertypageinfo.htm
tech.root: ad
ms.assetid: 1f8313cd-5cbe-440b-bcf9-de835f2b4f4a
ms.date: 12/05/2018
ms.keywords: '*LPDSPROPERTYPAGEINFO, DSPROPERTYPAGEINFO, DSPROPERTYPAGEINFO structure [Active Directory], LPDSPROPERTYPAGEINFO, LPDSPROPERTYPAGEINFO structure pointer [Active Directory], _glines_dspropertypageinfo, ad.dspropertypageinfo, dsclient/DSPROPERTYPAGEINFO, dsclient/LPDSPROPERTYPAGEINFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DSPROPERTYPAGEINFO, *LPDSPROPERTYPAGEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDSPROPERTYPAGEINFO
 - dsclient/LPDSPROPERTYPAGEINFO
 - DSPROPERTYPAGEINFO
 - dsclient/DSPROPERTYPAGEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsclient.h
api_name:
 - DSPROPERTYPAGEINFO
---

# DSPROPERTYPAGEINFO structure


## -description

The <b>DSPROPERTYPAGEINFO</b> structure is used by an Active Directory property sheet extension to obtain static registration data for the extension. This structure is  supplied by the <a href="/windows/desktop/AD/cfstr-dspropertypageinfo">CFSTR_DSPROPERTYPAGEINFO</a> clipboard format.

## -struct-fields

### -field offsetString

Contains the offset, in bytes, from the start of the <b>DSPROPERTYPAGEINFO</b> structure to a NULL-terminated, Unicode string that contains the optional data stored for the extension.

## -remarks

The  <b>DSPROPETYPAGEINFO</b> structure contains the optional string that the extension added to the <b>adminPropertySheet</b> and/or <b>shellPropertySheet</b> attributes when the extension was registered. For more information about how this string is set, see <a href="/windows/desktop/AD/registering-the-property-page-com-object-in-a-display-specifier">Registering the Property Page COM Object in a Display Specifier</a>.

## -see-also

<a href="/windows/desktop/AD/cfstr-dspropertypageinfo">CFSTR_DSPROPERTYPAGEINFO</a>



<a href="/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>



<a href="/windows/desktop/AD/registering-the-property-page-com-object-in-a-display-specifier">Registering the Property Page COM Object in a Display Specifier</a>


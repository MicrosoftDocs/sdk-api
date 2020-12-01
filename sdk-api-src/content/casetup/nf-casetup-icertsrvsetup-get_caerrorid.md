---
UID: NF:casetup.ICertSrvSetup.get_CAErrorId
title: ICertSrvSetup::get_CAErrorId (casetup.h)
description: Gets the ID for additional error information related to a failed certification authority (CA) specification.
helpviewer_keywords: ["CAErrorId property [Security]","CAErrorId property [Security]","ICertSrvSetup interface","ICertSrvSetup interface [Security]","CAErrorId property","ICertSrvSetup.CAErrorId","ICertSrvSetup.get_CAErrorId","ICertSrvSetup::CAErrorId","ICertSrvSetup::get_CAErrorId","IDS_ERR_CREATE_DIR","IDS_IDINFO_CAEXISTINDS","IDS_PATH_TOO_LONG_CANAME","IDS_PATH_TOO_LONG_DIRECTORY","IDS_STORELOC_PATHTOOLONG","IDS_STORELOC_UNCMUSTEXIST","IDS_WRN_DBFILEINUSE","IDS_WRN_DBSPECIALCHARACTERS","IDS_WRN_IDINFO_INVALIDDNEX","IDS_WRN_KEYNAMETOOLONG","IDS_WRN_OVERWRITEEXISTINGKEY","IDS_WRN_STORELOC_DB_FULLPATH","IDS_WRN_STORELOC_EXISTINGDB","IDS_WRN_STORELOC_LOG_FULLPATH","IDS_WRN_STORELOC_SHAREDFOLDER_FULLPATH","IDS_WRN_UNICODESTRINGENCODING","casetup/ICertSrvSetup::CAErrorId","casetup/ICertSrvSetup::get_CAErrorId","get_CAErrorId","security.icertsrvsetup_caerrorid"]
old-location: security\icertsrvsetup_caerrorid.htm
tech.root: security
ms.assetid: 462fb4a6-2aad-46d4-98e0-32c095eff5c7
ms.date: 12/05/2018
ms.keywords: CAErrorId property [Security], CAErrorId property [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],CAErrorId property, ICertSrvSetup.CAErrorId, ICertSrvSetup.get_CAErrorId, ICertSrvSetup::CAErrorId, ICertSrvSetup::get_CAErrorId, IDS_ERR_CREATE_DIR, IDS_IDINFO_CAEXISTINDS, IDS_PATH_TOO_LONG_CANAME, IDS_PATH_TOO_LONG_DIRECTORY, IDS_STORELOC_PATHTOOLONG, IDS_STORELOC_UNCMUSTEXIST, IDS_WRN_DBFILEINUSE, IDS_WRN_DBSPECIALCHARACTERS, IDS_WRN_IDINFO_INVALIDDNEX, IDS_WRN_KEYNAMETOOLONG, IDS_WRN_OVERWRITEEXISTINGKEY, IDS_WRN_STORELOC_DB_FULLPATH, IDS_WRN_STORELOC_EXISTINGDB, IDS_WRN_STORELOC_LOG_FULLPATH, IDS_WRN_STORELOC_SHAREDFOLDER_FULLPATH, IDS_WRN_UNICODESTRINGENCODING, casetup/ICertSrvSetup::CAErrorId, casetup/ICertSrvSetup::get_CAErrorId, get_CAErrorId, security.icertsrvsetup_caerrorid
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertSrvSetup::get_CAErrorId
 - casetup/ICertSrvSetup::get_CAErrorId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.CAErrorId
 - ICertSrvSetup.get_CAErrorId
---

# ICertSrvSetup::get_CAErrorId


## -description

The <b>CAErrorId</b> property gets the ID for additional error information related to a failed <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) specification. Any method call on the parent object resets this property.

This property is read-only.

## -parameters

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>
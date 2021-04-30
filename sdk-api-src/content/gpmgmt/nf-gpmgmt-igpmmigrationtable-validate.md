---
UID: NF:gpmgmt.IGPMMigrationTable.Validate
title: IGPMMigrationTable::Validate (gpmgmt.h)
description: Validates the migration table.
helpviewer_keywords: ["GPMMigrationTable class [GPMC]","Validate method","IGPMMigrationTable interface [GPMC]","Validate method","IGPMMigrationTable.Validate","IGPMMigrationTable::Validate","Validate","Validate method [GPMC]","Validate method [GPMC]","GPMMigrationTable class","Validate method [GPMC]","IGPMMigrationTable interface","gpmc.igpmmigrationtable_validate","gpmgmt/IGPMMigrationTable::Validate"]
old-location: gpmc\igpmmigrationtable_validate.htm
tech.root: gpmc
ms.assetid: 1b442155-3dd7-4a74-ad33-db79114459ac
ms.date: 12/05/2018
ms.keywords: GPMMigrationTable class [GPMC],Validate method, IGPMMigrationTable interface [GPMC],Validate method, IGPMMigrationTable.Validate, IGPMMigrationTable::Validate, Validate, Validate method [GPMC], Validate method [GPMC],GPMMigrationTable class, Validate method [GPMC],IGPMMigrationTable interface, gpmc.igpmmigrationtable_validate, gpmgmt/IGPMMigrationTable::Validate
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMMigrationTable::Validate
 - gpmgmt/IGPMMigrationTable::Validate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMMigrationTable.Validate
 - GPMMigrationTable.Validate
---

# IGPMMigrationTable::Validate


## -description

Validates the migration table.

## -parameters

### -param ppResult [out]

Reference to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface. The <b>Result</b> property references whether the validation is successful. The <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmessage">Status</a> property references the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> that contains the validation errors or warnings.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object. The <b>Result</b> property references whether the validation was successful. The <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmessage">Status</a> property references the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">GPMStatusMsgCollection</a> that contains the validation errors or warnings.

<h3>VB</h3>
Returns a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object. The <b>Result</b> property references whether the validation was successful. The <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmessage">Status</a> property references the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">GPMStatusMsgCollection</a> that contains the validation errors or warnings.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMMigrationTable</a>
---
UID: NF:gpmgmt.IGPMSOM.GetSecurityInfo
title: IGPMSOM::GetSecurityInfo (gpmgmt.h)
description: Returns an object that represents the collection of GPMPermission objects for the scope of management (SOM).
helpviewer_keywords: ["GPMSOM class [GPMC]","GetSecurityInfo method","GetSecurityInfo","GetSecurityInfo method [GPMC]","GetSecurityInfo method [GPMC]","GPMSOM class","GetSecurityInfo method [GPMC]","IGPMSOM interface","IGPMSOM interface [GPMC]","GetSecurityInfo method","IGPMSOM.GetSecurityInfo","IGPMSOM::GetSecurityInfo","_win32_igpmsom_getsecurityinfo","gpmc.igpmsom_getsecurityinfo","gpmgmt/IGPMSOM::GetSecurityInfo"]
old-location: gpmc\igpmsom_getsecurityinfo.htm
tech.root: gpmc
ms.assetid: 7b120bf6-17f8-43d7-a27c-b7674535c1d3
ms.date: 12/05/2018
ms.keywords: GPMSOM class [GPMC],GetSecurityInfo method, GetSecurityInfo, GetSecurityInfo method [GPMC], GetSecurityInfo method [GPMC],GPMSOM class, GetSecurityInfo method [GPMC],IGPMSOM interface, IGPMSOM interface [GPMC],GetSecurityInfo method, IGPMSOM.GetSecurityInfo, IGPMSOM::GetSecurityInfo, _win32_igpmsom_getsecurityinfo, gpmc.igpmsom_getsecurityinfo, gpmgmt/IGPMSOM::GetSecurityInfo
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
 - IGPMSOM::GetSecurityInfo
 - gpmgmt/IGPMSOM::GetSecurityInfo
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
 - IGPMSOM.GetSecurityInfo
 - GPMSOM.GetSecurityInfo
---

# IGPMSOM::GetSecurityInfo


## -description

Returns an object that represents the collection of 
 <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">GPMPermission</a>  objects for the scope of management (SOM).

## -parameters

### -param ppSecurityInfo [out]

Address of a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">GPMSecurityInfo</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">GPMSecurityInfo</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">GPMPermission</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>
---
UID: NN:gpmgmt.IGPMStarterGPO
title: IGPMStarterGPO (gpmgmt.h)
description: The IGPMStarterGPO interface supports methods that enable you to manage Starter Group Policy Objects (GPOs) in the directory service.
helpviewer_keywords: ["IGPMStarterGPO","IGPMStarterGPO interface [GPMC]","IGPMStarterGPO interface [GPMC]","described","gpmc.igpmstartergpo","gpmgmt/IGPMStarterGPO"]
old-location: gpmc\igpmstartergpo.htm
tech.root: gpmc
ms.assetid: 5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17
ms.date: 12/05/2018
ms.keywords: IGPMStarterGPO, IGPMStarterGPO interface [GPMC], IGPMStarterGPO interface [GPMC],described, gpmc.igpmstartergpo, gpmgmt/IGPMStarterGPO
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
 - IGPMStarterGPO
 - gpmgmt/IGPMStarterGPO
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
 - IGPMStarterGPO
---

# IGPMStarterGPO interface


## -description

The 
<b>IGPMStarterGPO</b> interface supports methods that enable you to manage Starter Group Policy Objects (GPOs) in the directory service.

Note that you cannot use this interface to manage local GPOs (LGPOs).

You can instantiate a <b>GPMStarterGPO</b> object by creating a new one with a call to 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain2-createstartergpo">IGPMDomain2::CreateStarterGPO</a>, retrieving an existing one with a call to 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain2-getstartergpo">IGPMDomain2::GetStarterGPO</a>, or by searching for one with a call to 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain2-searchstartergpos">IGPMDomain2::SearchStarterGPOs</a>. After creating the object, you can query the GPO and set properties related to the GPO.

## -inheritance

The <b>IGPMStarterGPO</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMStarterGPO</b> also has these types of members:

## -remarks

The <b>GPMStarterGPO</b> object is analogous to the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo2">GPMGPO2</a> object. The <b>GPMStarterGPO</b> object represents a single instance of a Starter Group Policy object (GPO).

The <b>IGPMStarterGPO</b> interface has three properties that do not have a counterpart in the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo2">IGPMGPO2</a> interface.

<ul>
<li>The <a href="/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Author</a> property contains the name of who created the Template.  This attribute is applicable to System Templates.  For custom Templates this attribute will be blank.  This attribute is read-only.</li>
<li>The <a href="/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Product</a> 
     property contains the name of the product that the Template is designed to manage.  For example a Template might ship to configure MS Office.  This attribute is applicable to System Templates.  For custom Templates this attribute will be blank.  This attribute is read-only.</li>
<li>The <a href="/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Type</a> 
     property is an enum value,  <a href="/windows/win32/api/gpmgmt/ne-gpmgmt-gpmstartergpotype">GPMStarterGPOType</a>, that specifies the type of the attribute.  The Type may be either a system  Starter Group Policy object or a custom Starter Group Policy object.</li>
</ul>
The <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-save">Save</a> method has no corresponding method in the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo2">IGPMGPO2</a> interface.  The <b>Save</b> method will generate a CAB file containing all the contents of a single Starter GPO.  The objective of this method is to allow a user to save a Starter GPO in a form that can be easily redistributed. There is no way to create a CAB file containing multiple Starter GPOs.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm2">IGPM2</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain2">IGPMDomain2</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">IGPMStarterGPOBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpocollection">IGPMStarterGPOCollection</a>

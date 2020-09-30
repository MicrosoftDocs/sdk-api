---
UID: NS:mmc._RESULT_VIEW_TYPE_INFO
title: RESULT_VIEW_TYPE_INFO (mmc.h)
description: The RESULT_VIEW_TYPE_INFO structure is introduced in MMC 2.0.
helpviewer_keywords: ["*PRESULT_VIEW_TYPE_INFO","MMC_VIEW_TYPE_HTML","MMC_VIEW_TYPE_LIST","MMC_VIEW_TYPE_OCX","RESULT_VIEW_TYPE_INFO","RESULT_VIEW_TYPE_INFO structure [MMC]","RVTI_LIST_OPTIONS_ALLOWPASTE","RVTI_LIST_OPTIONS_EXCLUDE_SCOPE_ITEMS_FROM_LIST","RVTI_LIST_OPTIONS_FILTERED","RVTI_LIST_OPTIONS_LEXICAL_SORT","RVTI_LIST_OPTIONS_MULTISELECT","RVTI_LIST_OPTIONS_NONE","RVTI_LIST_OPTIONS_OWNERDATALIST","RVTI_LIST_OPTIONS_USEFONTLINKING","RVTI_OCX_OPTIONS_CACHE_OCX","RVTI_OCX_OPTIONS_NOLISTVIEW","RVTI_OCX_OPTIONS_NONE","_slate_result_view_type_info","mmc.result_view_type_info","mmc/RESULT_VIEW_TYPE_INFO"]
old-location: mmc\result_view_type_info.htm
tech.root: mmc
ms.assetid: 50357902-6999-4d65-8e12-81277b66d5ee
ms.date: 12/05/2018
ms.keywords: '*PRESULT_VIEW_TYPE_INFO, MMC_VIEW_TYPE_HTML, MMC_VIEW_TYPE_LIST, MMC_VIEW_TYPE_OCX, RESULT_VIEW_TYPE_INFO, RESULT_VIEW_TYPE_INFO structure [MMC], RVTI_LIST_OPTIONS_ALLOWPASTE, RVTI_LIST_OPTIONS_EXCLUDE_SCOPE_ITEMS_FROM_LIST, RVTI_LIST_OPTIONS_FILTERED, RVTI_LIST_OPTIONS_LEXICAL_SORT, RVTI_LIST_OPTIONS_MULTISELECT, RVTI_LIST_OPTIONS_NONE, RVTI_LIST_OPTIONS_OWNERDATALIST, RVTI_LIST_OPTIONS_USEFONTLINKING, RVTI_OCX_OPTIONS_CACHE_OCX, RVTI_OCX_OPTIONS_NOLISTVIEW, RVTI_OCX_OPTIONS_NONE, _slate_result_view_type_info, mmc.result_view_type_info, mmc/RESULT_VIEW_TYPE_INFO'
req.header: mmc.h
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
req.typenames: RESULT_VIEW_TYPE_INFO, *PRESULT_VIEW_TYPE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RESULT_VIEW_TYPE_INFO
 - mmc/_RESULT_VIEW_TYPE_INFO
 - PRESULT_VIEW_TYPE_INFO
 - mmc/PRESULT_VIEW_TYPE_INFO
 - RESULT_VIEW_TYPE_INFO
 - mmc/RESULT_VIEW_TYPE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - RESULT_VIEW_TYPE_INFO
---

# RESULT_VIEW_TYPE_INFO structure


## -description

The <b>RESULT_VIEW_TYPE_INFO</b> structure is introduced in MMC 2.0.

The <b>RESULT_VIEW_TYPE_INFO</b> structure is used in calls to 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a> and 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-restoreresultview">IComponent2::RestoreResultView</a>. A snap-in uses these two methods to include a result view in the navigational order maintained by MMC's 
<b>Back</b>/<b>Forward</b> buttons.

## -struct-fields

### -field pstrPersistableViewDescription

Snap-in-provided identifier for this view type. When implementing <a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a>, this member must contain a valid view description string; otherwise, MMC will not initialize your snap-in. Additionally, this value must be created by means of <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. It will be freed by MMC, not the snap-in.

### -field eViewType

<a href="/windows/desktop/api/mmc/ne-mmc-mmc_view_type">MMC_VIEW_TYPE</a> enumeration value specifying the view type. This member is the structure's union discriminator and determines which members of the union are valid. This member is one of the following values.



#### MMC_VIEW_TYPE_LIST

This view is a list view.



#### MMC_VIEW_TYPE_HTML

This view is an HTML view.



#### MMC_VIEW_TYPE_OCX

This view is an OCX (ActiveX control) view.

### -field dwMiscOptions

A value that specifies whether the view contains list views. If this value is <b>RVTI_MISC_OPTIONS_NOLISTVIEWS</b>, no list views are contained in the view (the console refrains from presenting standard list view choices on the <b>View</b> menu). Otherwise, this value is zero.

### -field dwListOptions

A value that specifies the list view options. Applies only when the <b>eViewType</b> member is <b>MMC_VIEW_TYPE_LIST</b>. This value can be one or more of the following values.



#### RVTI_LIST_OPTIONS_NONE

No view options selected. This is the default view option.



#### RVTI_LIST_OPTIONS_OWNERDATALIST

A value that specifies that the result pane list view should be a virtual list.



#### RVTI_LIST_OPTIONS_MULTISELECT

Allows multiple item selections in the result pane view.



#### RVTI_LIST_OPTIONS_FILTERED

Notifies MMC that the snap-in supports filtered views. See <a href="/previous-versions/windows/desktop/mmc/adding-filtered-views">Adding Filtered Views</a>.



#### RVTI_LIST_OPTIONS_USEFONTLINKING

Uses font linking on result items (for multilingual support). Font linking is a feature installed on systems with Microsoft Internet Explorer version 4.0 or later. Given a Unicode string, the font linking feature determines the best font for that displays that string. For example, to populate a list view with server names in both Japanese and Russian, you would set the font linking view options, and MMC would determine an appropriate font. In the default setting, font linking is not enabled because it can cause a short delay while MMC searches for the appropriate font.



#### RVTI_LIST_OPTIONS_EXCLUDE_SCOPE_ITEMS_FROM_LIST

Causes MMC to hide scope items in the view; this applies to standard list views. Scope items are hidden in virtual list views.



#### RVTI_LIST_OPTIONS_LEXICAL_SORT

Causes MMC to lexically sort all scope items (including extensions) first, followed by all result items; this applies to standard list views. The <a href="/windows/desktop/api/mmc/nn-mmc-iresultdatacompare">IResultDataCompare</a> and <a href="/windows/desktop/api/mmc/nn-mmc-iresultdatacompareex">IResultDataCompareEx</a> interfaces are ignored when this value is set.



#### RVTI_LIST_OPTIONS_ALLOWPASTE

Informs MMC that the result pane item is a drop target (see <a href="/previous-versions/windows/desktop/mmc/using-drag-and-drop-to-result-pane-items">Using Drag and Drop to Result Pane Items</a>).

### -field dwHTMLOptions

Applies only when <b>eViewType</b> is <b>MMC_VIEW_TYPE_HTML</b>. This value is reserved for future use and must be zero.

### -field pstrURL

The URL for the HTML view. This parameter applies only when the <b>eViewType</b> member is <b>MMC_VIEW_TYPE_HTML</b>.

### -field dwOCXOptions

Applies only when the <b>eViewType</b> member is <b>MMC_VIEW_TYPE_OCX</b>. This value can be one or more of the following values.

<div class="alert"><b>Note</b>  Once the OCX caching option has been set (either by using or not using the <b>RVTI_OCX_OPTIONS_CACHE_OCX</b> flag), the option choice for this instance of the snap-in must not be changed.</div>
<div> </div>


#### RVTI_OCX_OPTIONS_NONE

No options are specified for the OCX view.



#### RVTI_OCX_OPTIONS_NOLISTVIEW

There is no list view in the OCX view.



#### RVTI_OCX_OPTIONS_CACHE_OCX

MMC will cache the OCX. If this value is specified, then the snap-in should maintain the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer for the OCX, so that if MMC calls <a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a> again, the snap-in returns the <b>IUnknown</b> pointer. MMC then identifies the cached OCX and reuses it. 
Be aware that OCXs are cached for each <a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> object, so the snap-in should create a different OCX for each <b>IComponent</b> object even if<b> RVTI_OCX_OPTIONS_CACHE_OCX</b> is set.

### -field pUnkControl

The <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer for the OCX. This parameter applies only when the <b>eViewType</b> member is <b>MMC_VIEW_TYPE_OCX</b>. When a snap-in implements <a href="/windows/desktop/api/mmc/nn-mmc-icomponent2">IComponent2</a> and has an OCX in the result pane, the snap-in must create the OCX during the call to <a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a> and return the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer (through <b>pUnkControl</b>) to MMC. The snap-in must also initialize the OCX. MMC will not send a <a href="/previous-versions/windows/desktop/mmc/mmcn-initocx">MMCN_INITOCX</a> notification to the snap-in.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-restoreresultview">IComponent2::RestoreResultView</a>



<a href="/previous-versions/windows/desktop/mmc/restoring-result-views">Restoring Result Views</a>



<a href="/previous-versions/windows/desktop/mmc/using-drag-and-drop-to-result-pane-items">Using Drag and Drop to Result Pane Items</a>
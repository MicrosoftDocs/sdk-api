---
UID: NF:reconcil.IReconcilableObject.Reconcile
title: IReconcilableObject::Reconcile (reconcil.h)
description: Reconciles the state of an object with one or more other objects. The reconciliation updates the internal state of the object by merging the states of all objects to form a combined state.
helpviewer_keywords: ["IReconcilableObject interface [Legacy Windows Environment Features]","Reconcile method","IReconcilableObject.Reconcile","IReconcilableObject::Reconcile","RECONCILEF_FEEDBACKWINDOWVALID","RECONCILEF_MAYBOTHERUSER","RECONCILEF_NORESIDUESOK","RECONCILEF_OMITSELFRESIDUE","RECONCILEF_ONLYYOUWERECHANGED","RECONCILEF_RESUMEDRECONCILIATION","RECONCILEF_YOUMAYDOTHEUPDATES","Reconcile","Reconcile method [Legacy Windows Environment Features]","Reconcile method [Legacy Windows Environment Features]","IReconcilableObject interface","_win32_IReconcilableObject_Reconcile","lwef.ireconcilableobject_reconcile","reconcil/IReconcilableObject::Reconcile","shell.ireconcilableobject_reconcile"]
old-location: lwef\ireconcilableobject_reconcile.htm
tech.root: lwef
ms.assetid: 6dfeb68e-fd23-4812-8a3c-ab27fc00a4ad
ms.date: 12/05/2018
ms.keywords: IReconcilableObject interface [Legacy Windows Environment Features],Reconcile method, IReconcilableObject.Reconcile, IReconcilableObject::Reconcile, RECONCILEF_FEEDBACKWINDOWVALID, RECONCILEF_MAYBOTHERUSER, RECONCILEF_NORESIDUESOK, RECONCILEF_OMITSELFRESIDUE, RECONCILEF_ONLYYOUWERECHANGED, RECONCILEF_RESUMEDRECONCILIATION, RECONCILEF_YOUMAYDOTHEUPDATES, Reconcile, Reconcile method [Legacy Windows Environment Features], Reconcile method [Legacy Windows Environment Features],IReconcilableObject interface, _win32_IReconcilableObject_Reconcile, lwef.ireconcilableobject_reconcile, reconcil/IReconcilableObject::Reconcile, shell.ireconcilableobject_reconcile
req.header: reconcil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IReconcilableObject::Reconcile
 - reconcil/IReconcilableObject::Reconcile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IReconcilableObject.Reconcile
---

# IReconcilableObject::Reconcile


## -description

Reconciles the state of an object with one or more other objects. The reconciliation updates the internal state of the object by merging the states of all objects to form a combined state.

## -parameters

### -param pInitiator

Type: <b><a href="/windows/desktop/lwef/ireconcileinitiator">IReconcileInitiator</a>*</b>

The address of the <a href="/windows/desktop/lwef/ireconcileinitiator">IReconcileInitiator</a> interface for the initiator of the reconciliation process. This parameter must not be <b>NULL</b>.

### -param dwFlags

Type: <b>DWORD</b>

The control flags for the reconciliation. This parameter may be zero or a combination of these values: 



#### RECONCILEF_FEEDBACKWINDOWVALID

The <i>hwndProgressFeedback</i> parameter is valid. 



#### RECONCILEF_MAYBOTHERUSER

The briefcase reconciler can prompt for user interaction if it is needed. Without this value, user interaction is not permitted. The <i>hwndOwner</i> parameter is valid. 



#### RECONCILEF_NORESIDUESOK

The briefcase reconciler can ignore requests for residues and carry out reconciliation. Reconcilers that do not support residues should check for this value whenever an initiator requests residues. Without this value, a reconciler that does not support residues must immediately return REC_E_NORESIDUES. 



#### RECONCILEF_OMITSELFRESIDUE

The briefcase reconciler can discard any residue associated with this object. Initiators typically use this value for reconciliations that loop from generation to generation. 



#### RECONCILEF_ONLYYOUWERECHANGED

The <b>Reconcile</b> method is being called to propagate changes in the changed object to other unchanged objects. This value will only be set if the following key exists in the registry.
					<pre><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <i>{CLSID of reconciler}</i>
         <b>SingleChangeHook</b></pre>


If this key is not present in the registry, the initiator carries out reconciliation by making the other unchanged objects binary identical copies of the changed object. The 
							<i>rgpmkOtherInput</i> monikers identify the other objects. This value will only be set in 
							<i>dwFlags</i> if RECONCILEF_YOUMAYDOTHEUPDATES is also set. If the briefcase reconciler completes the updates itself successfully, REC_S_IDIDTHEUPDATES should be returned and the variable pointed to by the 
							<i>plOutIndex</i> parameter should be set to -1L. Note that S_OK should not be returned on success if this value is set in 
							<i>dwFlags</i>. The initiator will not save the source object's storage if <b>Reconcile</b> returns REC_S_IDIDTHEUPDATES. If the reconciler wishes to fall back to the initiator's bit copy implementation, it may return S_FALSE. 



#### RECONCILEF_RESUMEDRECONCILIATION

The briefcase reconciler should resume reconciliation, using the partial residues provided. Without this value, the reconciler should ignore any "considered but rejected" information in any of the input versions. 



#### RECONCILEF_YOUMAYDOTHEUPDATES

The briefcase reconciler can perform the updates. Without this value, the reconciler cannot perform the updates. If reconciliation is completed successfully, the reconciler should return REC_S_IDIDTHEUPDATES if it performed the updates or S_OK if it did not perform the updates.

### -param hwndOwner

Type: <b>HWND</b>

A handle to the window to be used as the parent for any child windows that the briefcase reconciler creates. This parameter is valid only if RECONCILEF_MAYBOTHERUSER is specified in 
					<i>dwFlags</i>.

### -param hwndProgressFeedback

Type: <b>HWND</b>

A handle to the progress feedback window to be displayed by the initiator. This parameter is valid only if RECONCILEF_FEEDBACKWINDOWVALID is specified in 
					<i>dwFlags</i>. The briefcase reconciler may call the 
					<b>SetWindowText</b> function using this window handle to display additional reconciliation status information to the user.

### -param ulcInput

Type: <b>ULONG</b>

The number of versions or partial residues specified in 
					<i>dwFlags</i>. This parameter must not be zero.

### -param rgpmkOtherInput

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>**</b>

The address of an array that contains the addresses of the monikers to use to access the versions or partial residues to be reconciled.

### -param plOutIndex

Type: <b>LONG*</b>

The address of the variable that receives an index value indicating whether the result of the reconciliation is identical to one of the initial versions. The variable is set to -1L if the reconciliation result is a combination of two or more versions. Otherwise, it is a zero-based index, with 0 indicating this object, 1 indicating the first version, 2 indicating the second version, and so on.

### -param pstgNewResidues

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>*</b>

The address of the 
					<b>IStorage</b> interface used to store the new residues. This parameter can be <b>NULL</b> to indicate that residues should not be saved.

### -param pvReserved

Type: <b>void*</b>

Reserved; must be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Reconciliation completed successfully, and the changes must be propagated to the other objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No reconciliation actions were performed. The briefcase reconciler wishes to fall back to the initiator's bit copy implementation. This value may only be returned if RECONCILEF_ONLYYOUWERECHANGED is set in 
										<i>dwFlags</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REC_S_IDIDTHEUPDATES</b></dt>
</dl>
</td>
<td width="60%">
Reconciliation was completed successfully, and all the objects involved (the object implementing the <a href="/windows/desktop/api/reconcil/nf-reconcil-ireconcilableobject-reconcile">Reconcile</a> method and all the other objects described by 
										<i>rgpmkOtherInput</i>) have been updated appropriately. The initiator does not need, therefore, to do anything further to propagate the changes. The variable pointed to by 
										<i>plOutIndex</i> should be set to -1L if <b>Reconcile</b> returns this value. The initiator will not save the source object's storage if <b>Reconcile</b> returns this value. This value may only be returned if RECONCILEF_YOUMAYDOTHEUPDATES was set in 
										<i>dwFlags</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REC_S_NOTCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The briefcase reconciler completed some, but not all, of the reconciliation. It may need user interaction. The changes will not be propagated to other objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REC_S_NOTCOMPLETEBUTPROPAGATE</b></dt>
</dl>
</td>
<td width="60%">
The briefcase reconciler completed some, but not all, of the reconciliation. It may need user interaction. The changes will be propagated to the other objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REC_E_NORESIDUES</b></dt>
</dl>
</td>
<td width="60%">
The briefcase reconciler does not support the generation of residues, so the request for residues is denied. The state of the object is unchanged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REC_E_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The briefcase reconciler stopped reconciliation in response to a termination request from the initiator (see <a href="/previous-versions/bb761345(v=vs.85)">SetAbortCallback</a> for more information). The state of the object is unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REC_E_TOODIFFERENT</b></dt>
</dl>
</td>
<td width="60%">
Reconciliation cannot be carried out because the provided document versions are too dissimilar.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REC_E_INEEDTODOTHEUPDATES</b></dt>
</dl>
</td>
<td width="60%">
The RECONCILEF_YOUMAYDOTHEUPDATES flag was not set when the object's <a href="/windows/desktop/api/reconcil/nf-reconcil-ireconcilableobject-reconcile">Reconcile</a> implementation was called; this implementation requires that this value be set in the 
										<i>dwFlags</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The object is an OLE embedded object that must be run before this operation can be carried out. The state of the object is unchanged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/reconcil/nn-reconcil-ireconcilableobject">IReconcilableObject</a>

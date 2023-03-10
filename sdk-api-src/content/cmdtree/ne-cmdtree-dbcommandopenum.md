---
UID: NE:cmdtree.DBCOMMANDOPENUM
title: DBCOMMANDOPENUM (cmdtree.h)
description: The DBCOMMANDOPENUM enumerated type contains a list of the possible command operators for nodes in a command tree.
helpviewer_keywords: ["DBCOMMANDOPENUM","DBCOMMANDOPENUM enumeration [Indexing Service]","See below.","_idxs_DBCOMMANDOPENUM","cmdtree/DBCOMMANDOPENUM","cmdtree/See below.","indexsrv.dbcommandopenum"]
old-location: indexsrv\dbcommandopenum.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_6yp9.htm
ms.date: 12/05/2018
ms.keywords: DBCOMMANDOPENUM, DBCOMMANDOPENUM enumeration [Indexing Service], See below., _idxs_DBCOMMANDOPENUM, cmdtree/DBCOMMANDOPENUM, cmdtree/See below., indexsrv.dbcommandopenum
req.header: cmdtree.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DBCOMMANDOPENUM
 - cmdtree/DBCOMMANDOPENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cmdtree.h
api_name:
 - DBCOMMANDOPENUM
---

# DBCOMMANDOPENUM enumeration


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBCOMMANDOPENUM</b> enumerated type contains a list of the possible command operators for nodes in a command tree.

## -enum-fields

### -field DBOP_scalar_constant:0

### -field DBOP_DEFAULT

### -field DBOP_NULL

### -field DBOP_bookmark_name

### -field DBOP_catalog_name

### -field DBOP_column_name

### -field DBOP_schema_name

### -field DBOP_outall_name

### -field DBOP_qualifier_name

### -field DBOP_qualified_column_name

### -field DBOP_table_name

### -field DBOP_nested_table_name

### -field DBOP_nested_column_name

### -field DBOP_row

### -field DBOP_table

### -field DBOP_sort

### -field DBOP_distinct

### -field DBOP_distinct_order_preserving

### -field DBOP_alias

### -field DBOP_cross_join

### -field DBOP_union_join

### -field DBOP_inner_join

### -field DBOP_left_semi_join

### -field DBOP_right_semi_join

### -field DBOP_left_anti_semi_join

### -field DBOP_right_anti_semi_join

### -field DBOP_left_outer_join

### -field DBOP_right_outer_join

### -field DBOP_full_outer_join

### -field DBOP_natural_join

### -field DBOP_natural_left_outer_join

### -field DBOP_natural_right_outer_join

### -field DBOP_natural_full_outer_join

### -field DBOP_set_intersection

### -field DBOP_set_union

### -field DBOP_set_left_difference

### -field DBOP_set_right_difference

### -field DBOP_set_anti_difference

### -field DBOP_bag_intersection

### -field DBOP_bag_union

### -field DBOP_bag_left_difference

### -field DBOP_bag_right_difference

### -field DBOP_bag_anti_difference

### -field DBOP_division

### -field DBOP_relative_sampling

### -field DBOP_absolute_sampling

### -field DBOP_transitive_closure

### -field DBOP_recursive_union

### -field DBOP_aggregate

### -field DBOP_remote_table

### -field DBOP_select

### -field DBOP_order_preserving_select

### -field DBOP_project

### -field DBOP_project_order_preserving

### -field DBOP_top

### -field DBOP_top_percent

### -field DBOP_top_plus_ties

### -field DBOP_top_percent_plus_ties

### -field DBOP_rank

### -field DBOP_rank_ties_equally

### -field DBOP_rank_ties_equally_and_skip

### -field DBOP_navigate

### -field DBOP_nesting

### -field DBOP_unnesting

### -field DBOP_nested_apply

### -field DBOP_cross_tab

### -field DBOP_is_NULL

### -field DBOP_is_NOT_NULL

### -field DBOP_equal

### -field DBOP_not_equal

### -field DBOP_less

### -field DBOP_less_equal

### -field DBOP_greater

### -field DBOP_greater_equal

### -field DBOP_equal_all

### -field DBOP_not_equal_all

### -field DBOP_less_all

### -field DBOP_less_equal_all

### -field DBOP_greater_all

### -field DBOP_greater_equal_all

### -field DBOP_equal_any

### -field DBOP_not_equal_any

### -field DBOP_less_any

### -field DBOP_less_equal_any

### -field DBOP_greater_any

### -field DBOP_greater_equal_any

### -field DBOP_anybits

### -field DBOP_allbits

### -field DBOP_anybits_any

### -field DBOP_allbits_any

### -field DBOP_anybits_all

### -field DBOP_allbits_all

### -field DBOP_between

### -field DBOP_between_unordered

### -field DBOP_match

### -field DBOP_match_unique

### -field DBOP_match_partial

### -field DBOP_match_partial_unique

### -field DBOP_match_full

### -field DBOP_match_full_unique

### -field DBOP_scalar_parameter

### -field DBOP_scalar_function

### -field DBOP_plus

### -field DBOP_minus

### -field DBOP_times

### -field DBOP_over

### -field DBOP_div

### -field DBOP_modulo

### -field DBOP_power

### -field DBOP_like

### -field DBOP_sounds_like

### -field DBOP_like_any

### -field DBOP_like_all

### -field DBOP_is_INVALID

### -field DBOP_is_TRUE

### -field DBOP_is_FALSE

### -field DBOP_and

### -field DBOP_or

### -field DBOP_xor

### -field DBOP_equivalent

### -field DBOP_not

### -field DBOP_implies

### -field DBOP_overlaps

### -field DBOP_case_condition

### -field DBOP_case_value

### -field DBOP_nullif

### -field DBOP_cast

### -field DBOP_coalesce

### -field DBOP_position

### -field DBOP_extract

### -field DBOP_char_length

### -field DBOP_octet_length

### -field DBOP_bit_length

### -field DBOP_substring

### -field DBOP_upper

### -field DBOP_lower

### -field DBOP_trim

### -field DBOP_translate

### -field DBOP_convert

### -field DBOP_string_concat

### -field DBOP_current_date

### -field DBOP_current_time

### -field DBOP_current_timestamp

### -field DBOP_content_select

### -field DBOP_content

### -field DBOP_content_freetext

### -field DBOP_content_proximity

### -field DBOP_content_vector_or

### -field DBOP_delete

### -field DBOP_update

### -field DBOP_insert

### -field DBOP_min

### -field DBOP_max

### -field DBOP_count

### -field DBOP_sum

### -field DBOP_avg

### -field DBOP_any_sample

### -field DBOP_stddev

### -field DBOP_stddev_pop

### -field DBOP_var

### -field DBOP_var_pop

### -field DBOP_first

### -field DBOP_last

### -field DBOP_in

### -field DBOP_exists

### -field DBOP_unique

### -field DBOP_subset

### -field DBOP_proper_subset

### -field DBOP_superset

### -field DBOP_proper_superset

### -field DBOP_disjoint

### -field DBOP_pass_through

### -field DBOP_defined_by_GUID

### -field DBOP_text_command

### -field DBOP_SQL_select

### -field DBOP_prior_command_tree

### -field DBOP_add_columns

### -field DBOP_column_list_anchor

### -field DBOP_column_list_element

### -field DBOP_command_list_anchor

### -field DBOP_command_list_element

### -field DBOP_from_list_anchor

### -field DBOP_from_list_element

### -field DBOP_project_list_anchor

### -field DBOP_project_list_element

### -field DBOP_row_list_anchor

### -field DBOP_row_list_element

### -field DBOP_scalar_list_anchor

### -field DBOP_scalar_list_element

### -field DBOP_set_list_anchor

### -field DBOP_set_list_element

### -field DBOP_sort_list_anchor

### -field DBOP_sort_list_element

### -field DBOP_alter_character_set

### -field DBOP_alter_collation

### -field DBOP_alter_domain

### -field DBOP_alter_index

### -field DBOP_alter_procedure

### -field DBOP_alter_schema

### -field DBOP_alter_table

### -field DBOP_alter_trigger

### -field DBOP_alter_view

### -field DBOP_coldef_list_anchor

### -field DBOP_coldef_list_element

### -field DBOP_create_assertion

### -field DBOP_create_character_set

### -field DBOP_create_collation

### -field DBOP_create_domain

### -field DBOP_create_index

### -field DBOP_create_procedure

### -field DBOP_create_schema

### -field DBOP_create_synonym

### -field DBOP_create_table

### -field DBOP_create_temporary_table

### -field DBOP_create_translation

### -field DBOP_create_trigger

### -field DBOP_create_view

### -field DBOP_drop_assertion

### -field DBOP_drop_character_set

### -field DBOP_drop_collation

### -field DBOP_drop_domain

### -field DBOP_drop_index

### -field DBOP_drop_procedure

### -field DBOP_drop_schema

### -field DBOP_drop_synonym

### -field DBOP_drop_table

### -field DBOP_drop_translation

### -field DBOP_drop_trigger

### -field DBOP_drop_view

### -field DBOP_foreign_key

### -field DBOP_grant_privileges

### -field DBOP_index_list_anchor

### -field DBOP_index_list_element

### -field DBOP_primary_key

### -field DBOP_property_list_anchor

### -field DBOP_property_list_element

### -field DBOP_referenced_table

### -field DBOP_rename_object

### -field DBOP_revoke_privileges

### -field DBOP_schema_authorization

### -field DBOP_unique_key

### -field DBOP_scope_list_anchor

### -field DBOP_scope_list_element

### -field DBOP_content_table

##### - See below.

## -remarks

The OLE DB Provider for Indexing Service does not support all the operators in this enumerated type. Indexing Service supports only elements in the list designated by the comment "// Indexing Service".

For information about individual operators, see <a href="/previous-versions/windows/desktop/indexsrv/data-manipulation-operators">Data Manipulation Operators</a>.
